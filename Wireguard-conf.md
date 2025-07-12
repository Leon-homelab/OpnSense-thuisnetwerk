# WireGuard-configuratie voor OPNsense met VLAN-segmentatie

## 1. Doel

Deze configuratie maakt veilige externe toegang mogelijk tot specifieke VLAN's via WireGuard. De configuratie beperkt toegang per VLAN en voorkomt ongewenste communicatie tussen netwerken.

---

## 2. Interfaceconfiguratie (OPNsense)

**Locatie:** VPN > WireGuard > Local > Instances

| Instelling       | Waarde             |
|------------------|--------------------|
| Enable           | ✔                  |
| Name             | `WG_OPNsense`      |
| Listen Port      | `51820`            |
| Tunnel Address   | `11.11.11.1/32`    |
| Private Key      | *(automatisch)*    |
| Public Key       | *(wordt getoond)*  |

> **Toelichting:**  
> De tunnel wordt gebruikt voor point-to-site VPN-verkeer. Subnet `11.11.11.0/24` wordt gereserveerd voor WireGuard clients.

---

## 3. Interface-koppeling

**Locatie:** Interfaces > Assignments

| Interface      | Network Port | Description |
|----------------|--------------|-------------|
| `WG_OPNsense`  | `wg0`        | WireGuard   |

Na het toevoegen:
- Enable de interface
- Geef het een beschrijvende naam (`WG_OPNsense`)
- Configureer niets onder IPv4, laat dit op `None`

---

## 4. Peer (clientconfiguratie)

**Locatie:** VPN > WireGuard > Local > Peers

| Instelling           | Waarde               |
|----------------------|----------------------|
| Name                 | `LeonPhone`          |
| Public Key (client)  | *(uit client export)*|
| Allowed IPs          | `11.11.11.2/32`      |
| Endpoint             | *(leeg laten)*       |
| Persistent Keepalive | `25`                 |

> **Toelichting:**  
> Alleen het opgegeven IP (11.11.11.2) wordt toegelaten. "Persistent Keepalive" houdt de tunnel actief bij NAT/firewall timeouts.

---

## 5. NAT-configuratie

**Locatie:** Firewall > NAT > Outbound  
Stel NAT in op **Hybrid Outbound NAT**.

### Toevoegen:

| Interface | Source           | Translation          |
|----------|------------------|----------------------|
| `WAN`    | `11.11.11.1/32`  | `Interface address`  |

> **Toelichting:**  
> Zonder deze regel kunnen WireGuard-clients geen toegang krijgen tot internet of andere netwerken via NAT.

---

## 6. Firewallregels: WG_IoT

**Locatie:** Firewall > Rules > WG_IoT

Regels (boven naar onder):

| Type   | Bron                  | Doel            | Protocol/Poort | Beschrijving                        |
|--------|-----------------------|------------------|----------------|-------------------------------------|
| Pass   | `WG_OPNsense net`     | `192.168.99.0/24`| *              | Allow toegang tot OPNsense          |
| Block  | `WG_OPNsense net`     | `RFC1918`        | *              | Block toegang tot interne netwerken |


> **Opmerking:**  
> Deze regels zorgen ervoor dat de WireGuard-client alleen bij OPNsense kan en niet bij andere VLANs (zoals LAN).

---

## 7. Clientconfiguratie (bijv. op telefoon)

**In de WireGuard-app:**

```ini
[Interface]
PrivateKey = <private key client>
Address = 11.11.11.2/32
DNS = 192.168.10.1

[Peer]
PublicKey = <public key OPNsense>
Endpoint = jouw-openbare-ip:51820
AllowedIPs = 192.168.99.0/24
PersistentKeepalive = 25


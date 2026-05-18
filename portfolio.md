# 💼 Portfolio: Leon's Homelab Project

## 📌 Over dit project

Dit project toont een volledig gesegmenteerd thuisnetwerk, opgebouwd met OPNsense. Binnen de omgeving zijn meerdere VLAN’s ingericht, VPN-toegang gerealiseerd met WireGuard en netwerkdetectie toegepast via Suricata en CrowdSec.

Daarnaast heb ik een Proxmox-server opgezet waarop verschillende containers draaien, waaronder Grafana voor firewall-visualisatie, Pi-hole voor DNS-gebaseerde ad-blocking en een back-upserver.

Het doel van dit project was om praktijkervaring op te doen met netwerkbeheer, systeembeheer, beveiliging en documentatie, met een sterke focus op best practices en security.

---

## 🧱 Gebruikte technologieën

- **Firewall**: OPNsense (met logging, NAT, port forwards, IDS)
- **Switching & VLAN**: TP-Link managed switch (802.1Q VLAN-tagging)
- **VPN**: WireGuard (met iOS-client)
- **Monitoring**: Suricata IDS/IPS, CrowdSec integratie
- **Netwerkarchitectuur**: Gescheiden netwerken (thuis, gasten, IoT, beheer)
- **Backups**: Opzetten en beheren van een backup-strategie
- **Datavisualisatie**: Datavisualisatie d.m.v. grafana
- **DNS Filtering**: Ad-Blocker d.m.v. Pi-hole

---

## 📁 Belangrijkste configuratieonderdelen

| Component       | Beschrijving                                         |
|------------------|------------------------------------------------------|
| VLAN-segmentatie | 12 subnetten met individuele firewallregels           |
| Firewallbeleid   | Expliciete exceptions + logging    |
| VPN-toegang      | Alleen toegang tot NAS, videodeurbel en sensor       |
| IDS/IPS          | Suricata actief op WAN-interface                     |
| DNS-filtering    | Pi-Hole filterd op DNS niveau                       |
| Logging          | Elke fallback block gelogd, gekoppeld aan CrowdSec  |

---

## 🧠 Wat dit project laat zien

- Begrip van netwerksegmentatie, subnetting en tagging
- Beheersing van firewall logica en VPN-configuratie
- Bekendheid met intrusion detection en gedragsanalyse
- Opzetten en beheren van een veilige netwerkarchitectuur
- Inrichten van DNS-filtering en advertentieblokkering
- Opzetten en beheren van een back-up strategie
- Advertentie blocker (Pi-hole) inrichten
- Capaciteit om complexe setups te documenteren
- Zelfstandig leren, testen, falen en verbeteren

---

## 📸 Screenshots en documentatie

Zie de bestanden in deze repository voor:
- Visueel schema van het netwerk (`networkdiagram.png`)
- Firewallregels en VLAN-indeling (`config/`)
- WireGuard setup met clients (`wireguard-config.md`)
- IDS en logginguitvoer (`crowdsec-suricata.md`)
- PVE (proxmox) dashboard (`PVE_start.png`)
- Grafana dashboard (`Grafana_firewall.png`)
- Pi-Hole dashboard (`Pi-hole_dashboard.png`)

---

## 📝 Over mij

Ik ben een ervaren operator die de overstap wil maken naar de IT. Mijn focus ligt op systeem/netwerkbeheer en security. Ik leer actief, documenteer alles nauwkeurig en werk graag aan gestructureerde systemen.

---

**GitHub**: [github.com/leon-homelab](https://github.com/leon-homelab)  
**E-mail**: leon.homelab@gmail.com

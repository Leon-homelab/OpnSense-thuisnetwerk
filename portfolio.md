# 💼 Portfolio: Leon's Homelab Project

## 📌 Over dit project

Dit project toont een volledig gesegmenteerd thuisnetwerk, opgezet met OPNsense, waarin meerdere VLAN’s zijn toegepast, VPN-toegang is gerealiseerd met WireGuard en detectie plaatsvindt via Suricata en CrowdSec. Het doel van dit project was om hands-on ervaring op te doen met netwerkbeheer, beveiliging en documentatie — met een focus op best practices.

---

## 🧱 Gebruikte technologieën

- **Firewall**: OPNsense (met logging, NAT, port forwards, IDS)
- **Switching & VLAN**: TP-Link managed switch (802.1Q VLAN-tagging)
- **VPN**: WireGuard (met iOS-client)
- **Monitoring**: Suricata IDS/IPS, CrowdSec integratie
- **Netwerkarchitectuur**: Gescheiden netwerken (thuis, gasten, IoT, beheer)

---

## 📁 Belangrijkste configuratieonderdelen

| Component       | Beschrijving                                         |
|------------------|------------------------------------------------------|
| VLAN-segmentatie | 7 subnetten met individuele firewallregels           |
| Firewallbeleid   | 'Block-first' met expliciete exceptions + logging    |
| VPN-toegang      | Alleen toegang tot NAS, videodeurbel en sensor       |
| IDS/IPS          | Suricata actief op WAN-interface                     |
| Logging          | Elke fallback block gelogd, gekoppeld aan CrowdSec  |

---

## 🧠 Wat dit project laat zien

- Begrip van netwerksegmentatie, subnetting en tagging
- Beheersing van firewall logica en VPN-configuratie
- Bekendheid met intrusion detection en gedragsanalyse
- Capaciteit om complexe setups te documenteren
- Zelfstandig leren, testen, falen en verbeteren

---

## 📸 Screenshots en documentatie

Zie de bestanden in deze repository voor:
- Visueel schema van het netwerk (`networkdiagram.png`)
- Firewallregels en VLAN-indeling (`config/`)
- WireGuard setup met clients (`wireguard-config.md`)
- IDS en logginguitvoer (`crowdsec-suricata.md`)

---

## 📝 Over mij

Ik ben een ervaren operator die de overstap wil maken naar de IT. Mijn focus ligt op systeem/netwerkbeheer en security. Ik leer actief, documenteer alles nauwkeurig en werk graag aan gestructureerde systemen.

---

**GitHub**: [github.com/leon-homelab](https://github.com/leon-homelab)  
**E-mail**: [optioneel]  

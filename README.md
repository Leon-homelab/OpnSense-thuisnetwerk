# 📡 Leon’s Homelab – IT Portfolio Project

Welkom bij mijn persoonlijke IT-homelab. Dit project toont hoe ik een professioneel gesegmenteerd netwerk heb opgezet met OPNsense, inclusief firewallregels, VLAN’s, WireGuard VPN en IDS/IPS. Dit lab dient als leeromgeving voor netwerkbeheer, cloudtechnologie en cybersecurity.

---

## 📘 Inhoud van dit repository

| Bestand / Map          | Beschrijving                                                 |
| ---------------------- | ------------------------------------------------------------ |
| `config/`              | Back-ups van OPNsense instellingen, firewallregels           |
| `networkdiagram.png`   | Visuele weergave van netwerkapparatuur     |
| `wireguard-config.md`  | Uitleg over de WireGuard setup en clientconfiguratie         |
| `crowdsec-suricata.md` | Logging en detectieregels binnen het netwerk                 |
| `portfolio.md`         | Portfolio-versie van het project voor sollicitatiedoeleinden |

---

## 📁 Mapstructuur

```text
leon-homelab/
├── config/
│   ├── opnsense-backup.xml
│   ├── firewallregels.md
│   └── vlans-overzicht.md
|   ├── mikrotikCSS610_VLAN.png
|   ├── mikrotikCSS610_VLANS.png
├── wireguard-config.md
├── crowdsec-suricata.md
├── networkdiagram.png
├── portfolio.md
|── OPNsense desktop
|── firewall log
└── README.md
```

---

## 🔧 Over dit project

Dit project demonstreert:

* VLAN-segmentatie met gescheiden netwerken voor thuisgebruik, gasten, media, NAS, deurbel&airco, IoT en beheer
* Twee access points die volgens het roamingprincipe werken
* Meerdere ssid's voor een correcte vlan toewijzing
* Firewallregels gebaseerd op een "Fallback block" met logging
* WireGuard VPN met beperkte toegang tot OPNsense GUI
* Integratie van IDS/IPS (Suricata) en gedragsschild (CrowdSec)
* Documentatie van het hele netwerk inclusief configuratiebestanden en scripts

---

## 🎓 Doelstellingen

* Leren werken met OPNsense in een productieachtige omgeving
* Begrip ontwikkelen van netwerksegmentatie, tagging en VLAN-routing
* Configureren van veilige externe toegang met VPN
* Detectie en logging automatiseren en analyseren
* Project documenteren in Markdown en GitHub

---

## 💼 Gebruik

1. Verken de configuratie in `config/`
2. Bekijk `wireguard-config.md` voor VPN-instructies
3. Raadpleeg `portfolio.md` voor een overzicht voor sollicitatiegebruik

---

## 🧠 Wat ik heb geleerd

* Segmentatie van netwerken verhoogt de veiligheid en beheersbaarheid
* VPN-toegang beperken tot noodzakelijke apparaten verhoogt controle
* IDS/IPS en gedragsschilden zijn onmisbaar voor detectie
* Documentatie en structuur helpen bij troubleshooting en overdraagbaarheid

---

## 📫 Contact

* GitHub: [github.com/leon-homelab](https://github.com/leon-homelab)
* E-mail: leon.homelab@gmail.com

*Laat gerust een issue of pull request achter als je feedback hebt of suggesties!*



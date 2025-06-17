OpnSense-thuisnetwerk

Leon’s Homelab – IT Portfolio Project

Welkom bij mijn persoonlijke IT-homelab. Dit project toont hoe ik een professioneel gesegmenteerd netwerk heb opgezet met OPNsense, inclusief firewallregels, VLAN’s, WireGuard VPN en IDS/IPS. Dit lab dient als leeromgeving voor netwerkbeheer, cloudtechnologie en cybersecurity.

📘 Inhoud van dit repository

Bestand / Map Beschrijving config/ Back-ups van OPNsense instellingen, firewallregels networkdiagram.png Visuele weergave van VLAN-structuur en netwerkapparatuur wireguard-config.md Uitleg over de WireGuard setup en clientconfiguratie crowdsec-suricata.md Logging en detectieregels binnen het netwerk portfolio.md Portfolio-versie van het project voor sollicitatiedoeleinden

🧱 Technische onderdelen

🔐 VLAN en firewall

VLAN10: Thuisnetwerk VLAN20: Gastnetwerk VLAN25: Smart TV's VLAN30: IoT-apparaten (zonnepanelen, printer) VLAN35: Eufi deurbel en Airco VLAN40: NAS VLAN50: Management-only (alleen toegankelijk vanuit VLAN10)

Firewallregels volgen het principe: Begin met BLOCK, dan laat toe wat nodig is, eindig met een gelogde fallback BLOCK.

🔌 VPN toegang (WireGuard)

Alleen toegang tot specifieke apparaten: NAS, Aico en Eufy deurbel. Externe verbinding via iOS getest Poort 51820/UDP opengezet op WAN met NAT-regel

🧠 IDS en gedragsschild

Suricata IDS actief op WAN-interface CrowdSec gekoppeld aan firewall logging

📷 Screenshots

VLAN-configuratie in OPNsense GUI WireGuard tunnelstatus Firewallregel per VLAN Loggingvoorbeelden met Suricata

🧪 Wat heb ik geleerd

Het belang van een goede netwerksegmentatie en tagging Werken met een firewall gebaseerd op “default deny” VPN-configuratie voor externe veilige toegang Detectie van netwerkgedrag en loganalyse

🚀 Hoe gebruik je dit repository?

Clone of download het project: git clone https://github.com/leon-homelab/opnsense-thuisnetwerk.git Bekijk de map config/ voor instellingen Lees wireguard-config.md om je eigen tunnel op te zetten Bekijk het portfolio-bestand voor documentatie

📫 Contact

GitHub: github.com/leon-homelab E-mail: [optioneel]

Laat gerust een issue of suggestie achter als je feedback hebt!

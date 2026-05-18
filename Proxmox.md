# 🖥️ Proxmox Virtual Environment

## 📌 Wat is Proxmox?

Binnen mijn homelab maak ik gebruik van Proxmox Virtual Environment (PVE) als virtualisatieplatform. Proxmox is een open-source hypervisor gebaseerd op Debian Linux waarmee zowel virtual machines (VM’s) als Linux Containers (LXC/CT’s) beheerd kunnen worden vanuit één centrale webinterface.

Met Proxmox kan ik verschillende diensten gescheiden draaien in eigen containers, wat zorgt voor betere beveiliging, overzicht en efficiënt resourcegebruik.

Belangrijke voordelen van Proxmox binnen mijn omgeving:

* Centrale beheeromgeving voor containers en virtual machines
* Efficiënt gebruik van hardwarebronnen
* Mogelijkheid tot snapshots en back-ups
* Ondersteuning voor netwerksegmentatie via VLAN’s
* Eenvoudig beheer via webinterface
* Schaalbaar en geschikt voor test- en productieomgevingen

---

# 📦 Containers (CT's)

Binnen Proxmox draaien meerdere Linux Containers (LXC’s) die ieder een eigen functie hebben binnen het netwerk.

## 📊 Grafana CT

Grafana wordt gebruikt voor het visualiseren van firewall- en netwerkdata. Hiermee kan ik logging en netwerkverkeer overzichtelijk monitoren via dashboards.

### Functionaliteiten

* Visualisatie van firewall logging
* Monitoring van netwerkactiviteit
* Dashboarding van systeeminformatie
* Analyse van netwerkverkeer

---

## 🛡️ Pi-hole CT

Pi-hole functioneert als DNS-gebaseerde advertentie- en trackingblocker binnen het netwerk.

### Functionaliteiten

* DNS filtering
* Advertentieblokkering
* Tracking protection
* Centrale DNS-server voor clients binnen het netwerk

---

## 💾 Backup Server CT

Deze container wordt gebruikt voor het beheren en opslaan van back-ups van configuraties en belangrijke data binnen het homelab.

### Functionaliteiten

* Automatische back-ups
* Opslag van configuratiebestanden
* Herstelmogelijkheden bij storingen
* Onderdeel van de back-upstrategie

---

## 📚 Calibre CT

Calibre is een lichtgewicht webapplicatie die een intuïtieve interface biedt voor het beheren, doorzoeken en lezen van een persoonlijke e-bookcollectie binnen het netwerk.

### Functionaliteiten

* Beheer van e-bookcollecties
* Centrale opslag van e-books
* Toegang via webinterface
* Ondersteuning voor verschillende e-bookformaten

---

## 📁 File browser CT

File Browser functioneert als een eenvoudige centrale fileserver binnen het netwerk. Hiermee kunnen bestanden centraal worden opgeslagen, beheerd en benaderd via een webinterface.

### Functionaliteiten

* Centrale opslag van bestanden
* Toegang via webinterface
* Bestandsbeheer binnen het netwerk
* Ondersteuning voor uploads en downloads

---

## 🐉 Kali Linux VM

Kali Linux wordt binnen het homelab gebruikt als security- en testomgeving voor netwerk- en beveiligingsanalyse. Deze virtual machine wordt ingezet voor het uitvoeren van securitytests en het analyseren van de netwerkconfiguratie.

### Functionaliteiten

* Netwerk- en securityanalyse
* Testen van firewallregels
* Vulnerability scanning
* Monitoring van netwerkverkeer
* Pentesting tools en security testing

---

# 🧠 Wat ik heb geleerd

Door het opzetten en beheren van Proxmox binnen mijn homelab heb ik ervaring opgedaan met:

* Linux beheer
* Containerisatie
* Virtualisatie
* Resource management
* Back-upstrategieën
* Netwerksegmentatie
* Monitoring en logging
* Security hardening
* Troubleshooting van complexe omgevingen

---

# 📸 Screenshots

Zie onderstaande bestanden binnen deze repository:

* `PVE_start.png`
* `Grafana_firewall.png`
* `Pi-hole_dashboard.png`

Deze screenshots geven een overzicht van de Proxmox omgeving en de actieve services.

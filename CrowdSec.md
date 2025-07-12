# 🔒 OPNsense CrowdSec Logging — VLAN300

Deze handleiding beschrijft de werking en logging van **CrowdSec** binnen OPNsense, specifiek gericht op **VLAN300** (je WAN-interface).

---

## 📋 Inhoud

- [📌 Wat is CrowdSec?](#-wat-is-crowdsec)
- [📈 Voorbeeld van gelogde verbindingen](#-voorbeeld-van-gelogde-verbindingen)
- [📡 Locatie in OPNsense](#-locatie-in-opnsense)
- [⚙️ Logging beheren](#️-logging-beheren)

---

## 📌 Wat is CrowdSec?

CrowdSec is een open-source IPS (Intrusion Prevention System) die verdachte IP's detecteert en automatisch blokkeert. Binnen OPNsense integreert het via firewallregels, doorgaans op de **WAN-interface**.

---

## 📈 Voorbeeld van gelogde verbindingen

In je firewall log verschijnen CrowdSec-blokkeringen als volgt:

- VLAN300 2025-07-10T21:22:42 162.216.150.21:53652 'WAN IP':4174 tcp CrowdSec (IPv4) in
- VLAN300 2025-07-10T21:22:36 147.185.132.134:51561 'WAN IP':9302 tcp CrowdSec (IPv4) in

---

## 📡 Locatie in OPNsense](#-locatie-in-opnsense

Firewall > Rules > VLAN300

Zoek naar regels met:
- Beschrijving: `CrowdSec (IPv4) in`
- Logging: ✅ Ingeschakeld
- Actie: **Block** of **Reject**

---

## ⚙️ Logging beheren](#️-logging-beheren

Wil je minder logging:
- Open de regel (`Edit`)
- Vink **"Log packets that are handled by this rule"** uit
- Opslaan & Apply Changes

Bekijk gelogde entries via:

Firewall > Log Files > Live View

Filter op:
- Interface: `VLAN300`
- Beschrijving: `"CrowdSec"` of `"4174"`/`"9302"` etc.

---


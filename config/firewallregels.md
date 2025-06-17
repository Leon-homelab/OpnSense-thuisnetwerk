# Firewallregels per VLAN (beknopt overzicht)

##VLAN 10 - LAN
• Allow LAN → Internet✅
• Allow LAN → NAS (192.168.40.x)✅
• Block LAN → VLAN 15 (TV), VLAN 20 (IoT), VLAN 30 (Gast), VLAN 50 (Beheer)❌

##VLAN 15 - TV
• Allow TV → Internet (HTTP/HTTPS)✅
• Block TV → alle andere VLANs❌

##VLAN 20 - IoT
• Allow IoT → Internet (HTTP/HTTPS)✅
• Block IoT → LAN, NAS, TV, Beheer❌

##VLAN 30 - Gast
• Allow Guest → Internet✅
• Block Guest → alle interne netwerken❌

##VLAN 40 - NAS
• Allow NAS → Internet (updates)✅
• Allow LAN → NAS✅
• Block NAS → IoT, Gast, TV❌

##VLAN 50 - Beheer
• Allow VLAN 50 → OPNsense beheer IP (bijv. 192.168.50.1)✅
• Block beheer vanaf alle andere VLANs naar OPNsense GUI/SSH❌
? Alleen VLAN 50 (poort 8) mag OPNsense beheren. Alle andere VLANs worden
geblokkeerd voor toegang tot OPNsense GUI en SSH

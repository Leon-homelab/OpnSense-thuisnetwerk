# Firewallregels per VLAN (beknopt overzicht)

## VLAN10 – Thuisnet
- Allow: naar internet
- Block: naar VLAN30, VLAN20
- Allow: naar VLAN50 (beheer)

## VLAN20 – Gast
- Allow: alleen naar internet (HTTP/HTTPS/DNS)
- Block: alle lokale netwerken

## VLAN30 – IoT
- Allow: naar internet
- Allow: naar specifieke IP’s (NAS, Eufy)
- Block: alle andere VLAN’s

## VLAN50 – Management
- Allow: alleen vanaf VLAN10
- Block: alle andere netwerken

## WireGuard
- Allow: toegang tot VLAN30 (NAS, camera’s)
- Block: alle andere VLAN’s

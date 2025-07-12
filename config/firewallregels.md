# Firewallregels voor een enkele VLAN's

##VLAN10: Thuisnetwerk
    | # | Action | Protocol | Source     | Destination   | Port(s) / Notes                        |
| - | ------ | -------- | ---------- | ------------- | -------------------------------------- |
| 1 | Pass   | Any      | VLAN99 net | VLAN10 net    | “Allow MGMT → LAN beheer”              |
| 2 | Pass   | TCP/UDP  | VLAN10 net | This Firewall | Dest port 53 → “Allow DNS to Unbound”  |
| 3 | Pass   | UDP      | VLAN10 net | any           | Dest port 123 → “Allow NTP”            |
| 4 | Pass   | Any      | VLAN10 net | !RFC1918      | “Allow LAN → Internet”                 |
| 5 | Block  | Any      | VLAN10 net | RFC1918       | “Block LAN → andere interne netwerken” |
| 6 | Block  | Any      | VLAN10 net | any           | “Fallback block all”                    |

##VLAN20: Gastnetwerk

##VLAN25: Media

##VLAN30: IP TV
| # | Action | Protocol | Source     | Destination   | Port(s) / Notes                        |
| - | ------ | -------- | ---------- | ------------- | -------------------------------------- |
| 1 | Pass   | Any      | VLAN99 net | VLAN30 net    | “Allow MGMT → IP TV beheer”              |
| 2 | Pass   | TCP/UDP  | VLAN30 net | This Firewall | Dest port 53 → “Allow DNS to Unbound”  |
| 3 | Pass   | UDP      | VLAN30 net | any           | Dest port 123 → “Allow NTP”            |
| 4 | Pass   | Any      | VLAN30 net | !RFC1918      | “Allow IP TV → Internet”                 |
| 5 | Block  | Any      | VLAN30 net | RFC1918       | “Block IP TV → andere interne netwerken” |
| 6 | Block  | Any      | VLAN30 net | any           | “Fallback block all”                    |


##VLAN35: Eufi deurbel en Airco

##VLAN40: NAS

##VLAN50: Domotica

##VLAN99: MGMT

##VLAN300: Odido WAN
| # | Action | Protocol | Source       | Destination    | Port(s) / Notes                        |
| - | ------ | -------- | ------------ | -------------- | -------------------------------------- |
| 1 | Pass   | UDP      | any          | VLAN300 address| 67-68 “DHCP client“              |
| 2 | Pass   | any      | This firewall| any            | “Firewall outbound“  |
| 3 | Pass   | ICMP     | any          | any            | “Ping toegestaan“            |
| 6 | Block  | Any      | VLAN25 net | any           | “Fallback block all”                    |





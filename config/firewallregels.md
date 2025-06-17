# Firewallregels per VLAN (beknopt overzicht)

##VLAN10: Thuisnetwerk

    -BLOCK: alles

    -ALLOW: naar internet

    -ALLOW: naar VLAN50

    -BLOCK: fallback block met log


##VLAN20: Gastnetwerk

    -BLOCK: alles

    -ALLOW: naar internet

    -BLOCK: fallback block met log

    

##VLAN25: Smart TV's

##VLAN30: IoT-apparaten (zonnepanelen, printer)

##VLAN35: Eufi deurbel en Airco

##VLAN40: NAS

##VLAN50: Management-only (alleen toegankelijk vanuit VLAN10)

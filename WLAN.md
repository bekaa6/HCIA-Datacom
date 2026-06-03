# HCIA-WLAN

**A1 and A2 Switch**
```shell
sysname A1
#
vlan batch 43 100 200
#
vlan 43
 description MGMT VLAN
vlan 100
 description Service VLAN
vlan 200
 description Service VLAN
#
interface Ethernet0/0/22
 port link-type trunk
 port trunk pvid vlan 43
 port trunk allow-pass vlan 43 100 200
#
interface GigabitEthernet0/0/1
 port link-type trunk
 port trunk allow-pass vlan 43 100 200
#
interface GigabitEthernet0/0/2
 port link-type trunk
 port trunk allow-pass vlan 43 100 200
#
```

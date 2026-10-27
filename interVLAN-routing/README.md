DEPARTMENT A SWITCH CLI CONFIGURATION:VLAN 10
enable
configure terminal

vlan 10
 name Department_A
exit

interface range fastEthernet 0/1-2
 switchport mode access
 switchport access vlan 10
exit

interface fastEthernet 0/24
 switchport mode access
 switchport access vlan 10
exit

end
copy running-config startup-config

DEPARTMENT B SWITCH CLI CONFIGURATION:VLAN 20

enable
configure terminal

vlan 20
 name Department_B
exit

interface range fastEthernet 0/1-2
 switchport mode access
 switchport access vlan 20
exit

interface fastEthernet 0/24
 switchport mode access
 switchport access vlan 20
exit

end
copy running-config startup-config

ROUTER CLI CONFIGURATION:


enable
configure terminal

interface gigabitEthernet 0/0
 ip address 192.168.10.1 255.255.255.0
 no shutdown
exit

interface gigabitEthernet 0/1
 ip address 192.168.20.1 255.255.255.0
 no shutdown
exit

end
copy running-config startup-config



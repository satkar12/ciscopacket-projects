enable
configure terminal

! Create an extended ACL
access-list 101 deny tcp host 192.168.1.10 host 10.10.10.1 eq 80

! Allow all other traffic
access-list 101 permit ip any any

! Apply ACL to router interface
interface fa0/0
ip access-group 101 in

exit
end
write memory

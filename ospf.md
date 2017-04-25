!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! OSPF CONFIGURATION !!!!!!!!!!!!!!!!!!!!!!!!!
!
! Turn on privileged commands
enable
!
! Enter configuration mode
configure terminal
!
! Enable a routing process
router ospf 1
!
! router-id for this OSPF process
! Example: 1.1.1.1
router-id <OSPF_ID>
!
! Calculate OSPF interface cost according to bandwidth
! Check out that every routers has the same reference bandwidth
!
auto-cost reference-bandwidth 10000
!
! OSPF area parameters
area 0 authentication message-digest
!
! Suppress routing updates on an interface
passive-interface <INTERFACE_NUMBER>
!
! Enable routing on an IP network
network <IP> <OSPF_WILD_CARD_BITS> area 0
!
! Exit from routing protocol configuration mode
exit
!
! Exit from configure mode
exit
!
! Reset OSPF process
clear ip ospf process
!
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! SAVING !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
!
! Copy from current system configuration to startup configuration
copy running-config startup-config

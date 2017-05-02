# OSPF troubleshooting

## Check the routing table

### Show IP-EIGRP routing table

    Router# show ip route ospf
    Router# show ipv6 route ospf

## Check contiguity establishment

### Show IP-OSPF neighbors

    Router# show ip ospf neighbors
    Router# show ipv6 ospf neighbors
    Router# show ip ospf interfaces

## Check OSPF configuration

### Show IP routing protocol process parameters and statistics

    Router# show ip protocols
    Router# show ipv6 protocols

### Show current operating configuration

    Router# running-config

### Disable OSPF

    Router(config)# no router ospf 1

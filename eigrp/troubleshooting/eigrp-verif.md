# EIGRP troubleshooting

## Check neighborhood table

### Show IP-EIGRP topology table

    Router# show ip eigrp topology

### Show all links in topology table

    Router# show ip eigrp topology all-links

## Check the routing table

### Show IP-EIGRP routing table

    Router# show ip route eigrp
    Router# show ipv6 route eigrp

## Check contiguity establishment

### Show IP-EIGRP neighbors

    Router# show ip eigrp neighbors
    Router# show ipv6 eigrp neighbors

## Check EIGRP configuration

### Show IP routing protocol process parameters and statistics

    Router# show ip protocols
    Router# show ipv6 protocols

### Show current operating configuration

    Router# running-config

### Disable EIGRP

    Router(config)# no router eigrp 1

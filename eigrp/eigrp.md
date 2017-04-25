# EIGRP configuration

## Enable a routing process

    Router(config)# router eigrp 1

## router-id for this EIGRP process

    Router(config-router)# router-id <EIGRP_ID>

## Suppress routing updates on an interface

    Router(config-router)# passive-interface <INTERFACE_NUMBER>

## Enable routing on an IP network

    Router(config-router)# network <IP> <EIGRP_WILD_CARD_BITS>

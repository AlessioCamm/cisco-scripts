# OSPF configuration

## Enable a routing process

    Router(config)# router ospf 1

## router-id for this OSPF process

    Router(config-router)# router-id <OSPF_ID>

## Calculate OSPF interface cost according to bandwidth

    Router(config-router)# auto-cost reference-bandwidth 10000

## OSPF area parameters

    Router(config-router)# area 0 authentication message-digest

## Suppress routing updates on an interface

    Router(config-router)# passive-interface <INTERFACE_NUMBER>

## Enable routing on an IP network

    Router(config-router)# network <IP> <OSPF_WILD_CARD_BITS> area 0

## Reset OSPF process

    Router# clear ip ospf process

# OSPF configuration

## Enable a routing process

    Router(config)# router ospf 1

## router-id for this OSPF process

    Router(config-router)# router-id <OSPF_ID>

## Calculate OSPF interface cost according to bandwidth

    Router(config)# auto-cost reference-bandwidth 10000

## OSPF area parameters

    Router(config)# area 0 authentication message-digest

## Suppress routing updates on an interface

    Router(config)# passive-interface <INTERFACE_NUMBER>

## Enable routing on an IP network

    Router(config)# network <IP> <OSPF_WILD_CARD_BITS> area 0

## Reset OSPF process

    Router# clear ip ospf process

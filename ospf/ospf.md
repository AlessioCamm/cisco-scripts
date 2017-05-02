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

## Global activation of MD5 authentication

    Router(config)# interface Serial <SERIAL_ID>
    Router(config-if)# ip ospf message-digest-key key md5 <MD5_PASSWORD

## Reset OSPF process

    Router# clear ip ospf process

## Go further (not necessary)

### Configures time between HELLO packets

    Router(config)# interfaces Serial <SERIAL_ID>
    Router(config-if)# ip ospf hello-interval <HELLO_VALUE>

### Configures interval after which a neighbor is declared dead

#### Be careful, dead interval > hello interval

    Router(config-if)# ip ospf dead-interval <DEAD_VALUE>

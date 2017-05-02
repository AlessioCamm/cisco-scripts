# EIGRP configuration

## Enable a routing process

    Router(config)# router eigrp 1

## router-id for this EIGRP process

    Router(config-router)# router-id <EIGRP_ID>

## Suppress routing updates on an interface

    Router(config-router)# passive-interface <INTERFACE_NUMBER>

## Enable routing on an IP network

    Router(config-router)# network <IP> <EIGRP_WILD_CARD_BITS>

## Configuring Authentication

### Creating a key and a key ring

    Router(config)# key chain <KEY_EIGRP>

### Configure a key identifier (need to be the same on every router)

    Router(config-keychain)# key 1

### Set key string

    Router(config-keychain-key)# key-string <PASSWORD>

### Enable authentication (to be done on all interfaces)

    Router(config)# interfaces Serial <SERIAL_ID>
    Router(config-if)# ip authentication mode eigrp <AS_NUMBER> md5
    Router(config-if)# ip authentication key-chain eigrp <AS_NUMBER> <KEY_EIGRP>

## Go further (not necessary)

### Perform address summarization

    Router(config-if)# ip summary-address eigrp as-number network-address subnet-mask

### Change EIGRP bandwidth (not available on Packet Tracer)

    Router(config-if)# interface serial <SERIAL_ID>
    Router(config-if)# bandwidth <BANDWIDTH>
    Router(config-if)# ip bandwidth-percent eigrp 1 <BANDWIDTH_PERCENT>

### Configures IP-EIGRP hello interval

    Router(config-if)# ip hello-interval eigrp <AS-NUMBER> <SECONDS>

### Configures IP-EIGRP hold-time (not available on Packet Tracer)

#### Be careful, hold-time > hello interval

    Router(config-if)# ip hold-time eigrp <AS-NUMBER> <SECONDS>

### Control load balancing variance

#### At equal cost (not available on Packet Tracer)

##### Editable

    Router(config-router)# maximum-paths value

##### Deactivation

    Router(config-router)# maximum-paths 1

#### At unequal cost

    Router(config-router)# variance <METRIC_VARIANCE_MULTIPLIER>

#### Restore balance at equal cost

    Router(config-router)# variance 1

#### Balance traffic in proportion to cost (not available on Packet Tracer)

    Router(config-router)# traffic-share balanced

# Routes configuration

## IPv4

### Assigns a route

    Router(config)# ip route <NETWORK_DESTINATION> <NETWORK_MASK> <NETWORK_TO_GO>

### Assigns a default route

    Router(config)# ip route 0.0.0.0 0.0.0.0 <NETWORK_TO_GOK>

## IPv6

### Enable IPv6

    Router(config)# ipv6 unicast-routing

### Assigns a route

    Router(config)# ipv6 route <NETWORK_DESTINATION/MASK> <NETWORK_TO_GO>

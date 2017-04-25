# GLBP configuration

## WARNING: GLBP isn't supported by Packet Tracer

### Enable GLBP and set the virtual IP address

    Router(config)# interface <INTERFACE_NUMBER>
    Router(config-if)# glbp 1 ip <GLBP_IP>

### Set priority level

    Router(config-if)# glbp 1 priority <GLBP_PRIORITY

### Overthrow lower priority Active routers

    Router(config-if)# glbp 1 preempt

### Set packets processing equitably

    Router(config-if)# glbp 1 load-balancing round-robin

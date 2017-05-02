# HSRP configuration

## Configuring the active router with the following hot standby attributes

### Enable HSRP and set the virtual IP address

    Router(config)# interface <INTERFACE_NUMBER>
    Router(config-if)# standby 1 ip address <HSRP_IP>

### Set priority level

    Router(config-if)# standby 1 priority <HSRP_PRIORITY>

### Overthrow lower priority Active routers

    Router(config-if)# standby 1 preempt

### Set group name (not available on Packet Tracer)

    Router(config-if)# standby 1 name <HSRP_NUMBER>


### Overthrow lower priority period Active routers (not available on Packet Tracer)

    Router(config-if)# standby 1 preempt delay minimum 300

## Configuring the standby router with the following hot standby attributes

### Enable HSRP and set the virtual IP address

    Router(config)# interface <INTERFACE_NUMBER>
    Router(config-if)# standby 1 ip address <HSRP_IP>

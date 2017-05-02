# Spanning Tree troubleshooting

## Useful commands to troubleshoot

### Show standby configuration

    Router# show standby

### Disable HSRP (to do on all routers)

    Router(config)# interface <INTERFACE_NUMBER>
    Router(config-if)# no standby 1

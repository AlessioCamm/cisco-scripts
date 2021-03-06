# Basic router configuration

## Set system's network name

    Router(config)# hostname <NAME_ROUTER>

## Disable IP Domain Name System hostname translation

    Router(config)# no ip domain-lookup

## Assign the privileged level secret

    Router(config)# enable secret <PASSWORD_PRIVILEGED>

## Encrypt system passwords

    Router(config)# service password-encryption

## Set Message of the Day banner

    Router(config)# banner motd # <BANNER_MOTD> #

## Configure a primary terminal line

    Router(config)# line console 0

### Set a password

    Router(config-line)# password <PASSWORD_CONSOLE>

### Set the EXEC timeout

    Router(config-line)# exec-timeout 2 30

### Enable password checking

    Router(config-line)# login

### Synchronized message output

    Router(config-line)# logging synchronous

## Configure a primary terminal line

    Router(config)# line vty 0 4

### Set a password

    Router(config-line)# password <PASSWORD_VTY>

### Set the EXEC timeout

    Router(config-line)# exec-timeout 2 30

### Enable password checking

    Router(config-line)# login

### Synchronized message output

    Router(config-line)# logging synchronous

## Copy from current system configuration to startup configuration

    Router# copy running-config startup-config

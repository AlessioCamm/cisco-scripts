# SSH configuration

## Define the default domain name

    Switch(config)# ip domain-name <NAME.com>

## Establish User Name Authentification

    Switch(config)# username <SSH_USERNAME> privilege 15 secret <SSH_PASSWORD>

## Configure virtual terminals

    Switch(config)# line vty 0 15

### Set SSH to use when connecting to the terminal server

    Switch(config-line)# transport input ssh

### Local password checking

    Switch(config-line)# login local

## Encryption module

    Switch(config)# crypto key generate rsa

## Specify SSH time-out interval

    Switch(config)# ip ssh time-out 30

## Specify number of authentication retries

    Switch(config)# ip ssh authentification-retries 3

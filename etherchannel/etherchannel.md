# EtherChannel configuration

## Set trunking mode to TRUNK unconditionally

    Switch(config-if)# interface range <BEGIN-END>
    Switch(config-range-if)# switchport mode trunk

## Prepare interface for PAgP protocol

    Switch(config-range-if)# channel-protocol pagp

## Etherchannel/port bundling configuration

    Switch(config-range-if)# channel-group 1 mode auto

## Enable the selected interface

    Switch(config-range-if)# no shutdown

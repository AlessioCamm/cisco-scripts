# EtherChannel configuration

## Set trunking mode to TRUNK unconditionally

    Switch(config-if)# interface range <BEGIN-END>
    Switch(config-range-if)# switchport mode trunk

## Set trunking native characteristics when interface is in trunking mode

    Switch(config-range-if)# switchport trunk native vlan 99

## Prepare interface for PAgP protocol

    Switch(config-range-if)# channel-protocol pagp

## Etherchannel/port bundling configuration

    Switch(config-range-if)# channel-group <GROUP_NUMBER> mode auto

## Enable the selected interface

    Switch(config-range-if)# no shutdown

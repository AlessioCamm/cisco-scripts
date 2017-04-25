# Spanning Tree configuration

## Assign Spanning Tree with Rapid PVST+

### Configure this switch as primary root for this spanning tree

    Switch(config)# spanning-tree vlan <BEGIN-END> root primary

### Per-Vlan rapid spanning tree mode

	Switch(config)# spanning-tree mode rapid-pvst

## Change an interface's spanning tree port priority

    Switch(config)# interface <INTERFACE_NUMBER>
    Switch(config-if)# spanning-tree vlan <BEGIN-END> port-priority <NUMBER>

## Enable an interface to move directly to forwarding on link up

    Switch(config-if)# interface <INTERFACE_NUMBER>
    Switch(config-if)# spanning-tree portfast

### Enable BPDU guard for this interface

    Switch(config-if)# spanning-tree bpduguard enable

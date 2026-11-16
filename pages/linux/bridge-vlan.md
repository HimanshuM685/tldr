# bridge vlan

> Manage VLAN filter entries of bridge ports.
> More information: <https://manned.org/bridge>.

- Show the VLANs configured on all bridge ports:

`bridge vlan show`

- Show the VLANs configured on a specific port:

`bridge vlan show dev {{eth0}}`

- Add a VLAN to a port:

`sudo bridge vlan add dev {{eth0}} vid {{10}}`

- Add a VLAN to a port as its native VLAN (untagged traffic is assigned to it):

`sudo bridge vlan add dev {{eth0}} vid {{20}} pvid untagged`

- Add a VLAN to the bridge device itself:

`sudo bridge vlan add dev {{br0}} vid {{10}} self`

- Remove a VLAN from a port:

`sudo bridge vlan del dev {{eth0}} vid {{10}}`

# bridge mdb

> Manage the multicast group database of a network bridge.
> More information: <https://manned.org/bridge>.

- Show all multicast group database entries:

`bridge mdb show`

- Show multicast group database entries of a specific bridge:

`bridge mdb show dev {{br0}}`

- Add a permanent multicast group entry for a port:

`sudo bridge mdb add dev {{br0}} port {{eth0}} grp {{239.1.1.1}} permanent`

- Add a permanent multicast group entry for a port on a specific VLAN:

`sudo bridge mdb add dev {{br0}} port {{eth0}} grp {{239.1.1.1}} permanent vid {{10}}`

- Delete a multicast group entry:

`sudo bridge mdb del dev {{br0}} port {{eth0}} grp {{239.1.1.1}}`

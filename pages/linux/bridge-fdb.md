# bridge fdb

> Manage the forwarding database (MAC address table) of a network bridge.
> More information: <https://manned.org/bridge>.

- Show all forwarding database entries:

`bridge fdb show`

- Show forwarding database entries of a specific bridge:

`bridge fdb show br {{br0}}`

- Show forwarding database entries of a specific port:

`bridge fdb show dev {{eth0}}`

- Add a static entry for a MAC address on a port:

`sudo bridge fdb add {{00:11:22:33:44:55}} dev {{eth0}} master static`

- Delete an entry for a MAC address on a port:

`sudo bridge fdb del {{00:11:22:33:44:55}} dev {{eth0}} master`

- Append a remote destination to a VXLAN device to flood unknown traffic to it:

`sudo bridge fdb append 00:00:00:00:00:00 dev {{vxlan0}} dst {{192.0.2.1}}`

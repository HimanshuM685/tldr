# bridge link

> Manage the ports of a network bridge.
> More information: <https://manned.org/bridge>.

- Show all bridge ports and their states:

`bridge link show`

- Show a specific bridge port:

`bridge link show dev {{eth0}}`

- Set the spanning tree path cost of a port:

`sudo bridge link set dev {{eth0}} cost {{4}}`

- Set the spanning tree priority of a port:

`sudo bridge link set dev {{eth0}} priority {{32}}`

- Enable or disable MAC address learning on a port:

`sudo bridge link set dev {{eth0}} learning {{on|off}}`

- Enable or disable hairpin mode (sending traffic back out the port it came in on):

`sudo bridge link set dev {{eth0}} hairpin {{on|off}}`

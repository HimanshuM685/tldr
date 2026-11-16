# tipc

> Configure the TIPC (Transparent Inter-Process Communication) protocol used for cluster communication.
> The `tipc` kernel module must be loaded first (`sudo modprobe tipc`).
> More information: <https://manned.org/tipc>.

- List the bearers (network interfaces used by TIPC):

`tipc bearer list`

- Enable TIPC on an Ethernet interface:

`sudo tipc bearer enable media eth device {{eth0}}`

- Disable TIPC on an Ethernet interface:

`sudo tipc bearer disable media eth device {{eth0}}`

- List the links to other cluster nodes:

`tipc link list`

- List the known cluster nodes:

`tipc node list`

- Show the name table (published service addresses):

`tipc nametable show`

- List the open TIPC sockets:

`tipc socket list`

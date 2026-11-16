# ip tunnel

> Manage IP tunnels, such as GRE, IPIP and SIT tunnels.
> More information: <https://manned.org/ip-tunnel>.

- Show all IPv4 tunnels:

`ip tunnel show`

- Show all IPv6 tunnels:

`ip -6 tunnel show`

- Create a GRE tunnel between two hosts:

`sudo ip tunnel add {{name}} mode gre remote {{203.0.113.1}} local {{198.51.100.1}} ttl {{255}}`

- Create a SIT tunnel to carry IPv6 traffic over IPv4:

`sudo ip tunnel add {{name}} mode sit remote {{203.0.113.1}} local {{198.51.100.1}}`

- Change the TTL of an existing tunnel:

`sudo ip tunnel change {{name}} ttl {{64}}`

- Delete a tunnel:

`sudo ip tunnel delete {{name}}`

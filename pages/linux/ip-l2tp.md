# ip l2tp

> Manage static L2TPv3 tunnels and sessions, which carry Ethernet frames over IP.
> More information: <https://manned.org/ip-l2tp>.

- Show all tunnels:

`ip l2tp show tunnel`

- Show all sessions:

`ip l2tp show session`

- Create a tunnel over UDP:

`sudo ip l2tp add tunnel tunnel_id {{1}} peer_tunnel_id {{1}} encap udp local {{192.0.2.1}} remote {{192.0.2.2}} udp_sport {{5000}} udp_dport {{5000}}`

- Create a session in a tunnel:

`sudo ip l2tp add session tunnel_id {{1}} session_id {{1}} peer_session_id {{1}}`

- Delete a session:

`sudo ip l2tp del session tunnel_id {{1}} session_id {{1}}`

- Delete a tunnel:

`sudo ip l2tp del tunnel tunnel_id {{1}}`

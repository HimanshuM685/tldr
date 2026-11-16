# ip tcp_metrics

> Manage the TCP metrics cache, which stores per-destination TCP parameters such as RTT.
> More information: <https://manned.org/ip-tcp_metrics>.

- Show all cached IPv4 TCP metrics:

`ip tcp_metrics show`

- Show all cached IPv6 TCP metrics:

`ip -6 tcp_metrics show`

- Show cached TCP metrics for a specific address prefix:

`ip tcp_metrics show {{192.0.2.0/24}}`

- Display cached TCP metrics for a specific address:

`ip tcp_metrics get {{192.0.2.1}}`

- Delete cached TCP metrics for a specific address:

`sudo ip tcp_metrics delete {{192.0.2.1}}`

- Delete all cached TCP metrics:

`sudo ip tcp_metrics flush all`

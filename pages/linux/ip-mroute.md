# ip mroute

> Display the multicast routing cache.
> More information: <https://manned.org/ip-mroute>.

- Show all IPv4 multicast routing cache entries:

`ip mroute show`

- Show all IPv6 multicast routing cache entries:

`ip -6 mroute show`

- Show multicast routing cache entries for a specific source:

`ip mroute show from {{192.0.2.1}}`

- Show multicast routing cache entries for a specific input interface:

`ip mroute show iif {{eth0}}`

- Show multicast routing cache entries of a specific table:

`ip mroute show table {{100}}`

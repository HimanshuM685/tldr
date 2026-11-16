# ip mrule

> Manage multicast routing policy rules.
> It takes the same arguments as `ip rule`.
> See also: `ip rule`, `ip mroute`.
> More information: <https://manned.org/ip-rule>.

- Show all IPv4 multicast routing rules:

`ip mrule show`

- Show all IPv6 multicast routing rules:

`ip -6 mrule show`

- Add a rule to look up multicast traffic from a specific network in another table:

`sudo ip mrule add from {{192.0.2.0/24}} table {{100}}`

- Delete a multicast routing rule:

`sudo ip mrule delete from {{192.0.2.0/24}} table {{100}}`

# ip nexthop

> Manage nexthop objects, which can be shared between routes.
> See also: `ip route`.
> More information: <https://manned.org/ip-nexthop>.

- Show all nexthops:

`ip nexthop show`

- Add a nexthop with a gateway address:

`sudo ip nexthop add id {{1}} via {{192.0.2.1}} dev {{eth0}}`

- Add a nexthop group that balances traffic across other nexthops:

`sudo ip nexthop add id {{10}} group {{1}}/{{2}}`

- Add a route that uses a nexthop:

`sudo ip route add {{198.51.100.0/24}} nhid {{1}}`

- Display a specific nexthop:

`ip nexthop get id {{1}}`

- Delete a specific nexthop:

`sudo ip nexthop delete id {{1}}`

- Delete all nexthops:

`sudo ip nexthop flush`

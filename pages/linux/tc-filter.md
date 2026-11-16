# tc filter

> Manage traffic control filters, which classify packets into classes or apply actions to them.
> See also: `tc`, `tc qdisc`, `tc class`.
> More information: <https://manned.org/tc>.

- Show the filters attached to an interface:

`tc filter show dev {{eth0}}`

- Show the ingress filters attached to an interface:

`tc filter show dev {{eth0}} ingress`

- Send packets to a specific destination network into a class:

`sudo tc filter add dev {{eth0}} parent {{1:}} protocol ip prio {{1}} u32 match ip dst {{192.168.1.0/24}} flowid {{1:10}}`

- Send packets to a specific destination port into a class:

`sudo tc filter add dev {{eth0}} parent {{1:}} protocol ip prio {{1}} u32 match ip dport {{22}} 0xffff flowid {{1:10}}`

- Drop incoming TCP packets on an interface (requires an ingress queueing discipline):

`sudo tc filter add dev {{eth0}} ingress protocol ip flower ip_proto tcp action drop`

- Delete all filters with a specific priority:

`sudo tc filter del dev {{eth0}} parent {{1:}} prio {{1}}`

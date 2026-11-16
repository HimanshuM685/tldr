# tc qdisc

> Manage queueing disciplines (qdiscs), which control how packets are queued and sent on a network interface.
> See also: `tc`, `tc class`, `tc filter`.
> More information: <https://manned.org/tc>.

- Show the queueing disciplines of all interfaces:

`tc qdisc show`

- Show the queueing disciplines of a specific interface with statistics:

`tc {{[-s|-statistics]}} qdisc show dev {{eth0}}`

- Set the root queueing discipline of an interface:

`sudo tc qdisc add dev {{eth0}} root {{fq_codel|pfifo_fast|htb|...}}`

- Replace the root queueing discipline of an interface, adding it if it does not exist:

`sudo tc qdisc replace dev {{eth0}} root netem delay {{100}}ms`

- Add an ingress queueing discipline to an interface:

`sudo tc qdisc add dev {{eth0}} ingress`

- Delete the root queueing discipline of an interface, restoring the default:

`sudo tc qdisc del dev {{eth0}} root`

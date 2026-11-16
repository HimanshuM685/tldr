# tc chain

> Manage traffic control filter chains, which group filters so that packets can jump between them.
> See also: `tc filter`.
> More information: <https://manned.org/tc>.

- Show the filter chains of the ingress of an interface:

`tc chain show dev {{eth0}} ingress`

- Add an empty filter chain to the ingress of an interface:

`sudo tc chain add dev {{eth0}} ingress chain {{1}}`

- Add a filter that sends TCP packets to another chain:

`sudo tc filter add dev {{eth0}} ingress chain 0 protocol ip flower ip_proto tcp action goto chain {{1}}`

- Show the filters in a specific chain:

`tc filter show dev {{eth0}} ingress chain {{1}}`

- Delete a filter chain and all its filters:

`sudo tc chain del dev {{eth0}} ingress chain {{1}}`

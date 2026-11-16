# ip vrf

> Run commands in a VRF (Virtual Routing and Forwarding) context and inspect VRF assignments.
> More information: <https://manned.org/ip-vrf>.

- Show all VRF devices:

`ip vrf show`

- Create a VRF device bound to a specific routing table:

`sudo ip link add {{vrf_name}} type vrf table {{10}}`

- Assign a network interface to a VRF:

`sudo ip link set dev {{eth0}} master {{vrf_name}}`

- Run a command in a VRF context:

`sudo ip vrf exec {{vrf_name}} {{command}}`

- Display the VRF of the current shell or of a specific process:

`ip vrf identify {{process_id}}`

- List the processes running in a VRF context:

`ip vrf pids {{vrf_name}}`

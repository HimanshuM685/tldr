# ip fou

> Manage receive ports for FOU (Foo over UDP) and GUE (Generic UDP Encapsulation) tunnels.
> More information: <https://manned.org/ip-fou>.

- Show all receive ports:

`ip fou show`

- Add a receive port for IPIP packets encapsulated in UDP:

`sudo ip fou add port {{5555}} ipproto 4`

- Add a receive port for GUE packets:

`sudo ip fou add port {{5555}} gue`

- Create an IPIP tunnel that sends packets encapsulated with FOU:

`sudo ip link add name {{tun1}} type ipip remote {{203.0.113.1}} local {{198.51.100.1}} encap fou encap-sport auto encap-dport {{5555}}`

- Delete a receive port:

`sudo ip fou del port {{5555}}`

# ip ntable

> Manage neighbor table parameters, such as ARP and NDP cache settings.
> See also: `ip neighbor`.
> More information: <https://manned.org/ip-ntable>.

- Show all neighbor tables and their parameters:

`ip ntable show`

- Show the neighbor table parameters of a specific interface:

`ip ntable show dev {{eth0}}`

- Show a specific neighbor table:

`ip ntable show name {{arp_cache|ndisc_cache}}`

- Show neighbor tables with statistics:

`ip {{[-s|-statistics]}} ntable show`

- Change a parameter of a neighbor table on a specific interface:

`sudo ip ntable change name {{arp_cache}} dev {{eth0}} {{queue}} {{8}}`

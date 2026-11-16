# ip addrlabel

> Manage IPv6 address labels, which influence source and destination address selection.
> More information: <https://manned.org/ip-addrlabel>.

- List all address labels:

`ip addrlabel list`

- Add a label to an address prefix:

`sudo ip addrlabel add prefix {{2001:db8::/32}} label {{100}}`

- Delete the label of an address prefix:

`sudo ip addrlabel del prefix {{2001:db8::/32}}`

- Delete all address labels:

`sudo ip addrlabel flush`

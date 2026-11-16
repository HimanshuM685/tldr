# ip ila

> Manage ILA (Identifier Locator Addressing) mappings, which translate IPv6 addresses for network virtualization.
> The `ila` kernel module must be loaded first (`sudo modprobe ila`).
> More information: <https://manned.org/ip-ila>.

- List all ILA mappings:

`ip ila list`

- Add a mapping that replaces one locator with another:

`sudo ip ila add loc_match {{2001:0:0:1}} loc {{2001:0:0:2}}`

- Add a mapping limited to a specific interface:

`sudo ip ila add loc_match {{2001:0:0:1}} loc {{2001:0:0:2}} dev {{eth0}}`

- Delete a mapping:

`sudo ip ila del loc_match {{2001:0:0:1}}`

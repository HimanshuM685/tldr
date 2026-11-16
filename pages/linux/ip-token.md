# ip token

> Manage IPv6 tokenized interface identifiers, which fix the host part of addresses created by stateless autoconfiguration.
> More information: <https://manned.org/ip-token>.

- List the tokens of all interfaces:

`ip token list`

- Display the token of a specific interface:

`ip token get dev {{eth0}}`

- Set the token of an interface:

`sudo ip token set {{::1a:2b:3c:4d}}/64 dev {{eth0}}`

- Remove the token of an interface:

`sudo ip token del dev {{eth0}}`

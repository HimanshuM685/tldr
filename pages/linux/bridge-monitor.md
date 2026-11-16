# bridge monitor

> Monitor bridge state changes as they happen.
> More information: <https://manned.org/bridge>.

- Monitor all bridge events:

`bridge monitor`

- Monitor only events of a specific type:

`bridge monitor {{link|fdb|mdb|vlan}}`

- Monitor all bridge events and print a timestamp before each one:

`bridge {{[-t|-timestamp]}} monitor`

# dcb

> Manage Data Center Bridging (DCB) settings of network interfaces, such as priority flow control.
> More information: <https://manned.org/dcb>.

- Show the Enhanced Transmission Selection (ETS) settings of an interface:

`dcb ets show dev {{eth0}}`

- Show the Priority Flow Control (PFC) settings of an interface:

`dcb pfc show dev {{eth0}}`

- Enable Priority Flow Control for a specific priority:

`sudo dcb pfc set dev {{eth0}} prio-pfc {{3}}:on`

- Show the application priority table of an interface:

`dcb app show dev {{eth0}}`

- Show the maximum rate settings of an interface:

`dcb maxrate show dev {{eth0}}`

- Show the ETS settings of an interface in pretty-printed JSON format:

`dcb {{[-j|-json]}} {{[-p|-pretty]}} ets show dev {{eth0}}`

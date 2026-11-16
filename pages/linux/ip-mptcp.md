# ip mptcp

> Manage MPTCP (Multipath TCP) path manager settings.
> More information: <https://manned.org/ip-mptcp>.

- Show all MPTCP endpoints:

`ip mptcp endpoint show`

- Add an endpoint that is used to create additional subflows:

`sudo ip mptcp endpoint add {{192.0.2.1}} dev {{eth0}} subflow`

- Delete a specific endpoint:

`sudo ip mptcp endpoint delete id {{1}}`

- Delete all endpoints:

`sudo ip mptcp endpoint flush`

- Show the MPTCP subflow and address limits:

`ip mptcp limits show`

- Set the MPTCP subflow and accepted address limits:

`sudo ip mptcp limits set subflow {{2}} add_addr_accepted {{2}}`

- Monitor MPTCP events:

`ip mptcp monitor`

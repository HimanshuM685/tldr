# ip macsec

> Manage MACsec (IEEE 802.1AE) devices, which encrypt Ethernet traffic between hosts on a LAN.
> More information: <https://manned.org/ip-macsec>.

- Show all MACsec devices:

`ip macsec show`

- Create a MACsec device on top of an interface, with encryption enabled:

`sudo ip link add link {{eth0}} {{macsec0}} type macsec encrypt on`

- Add a transmit security association with a 128-bit key:

`sudo ip macsec add {{macsec0}} tx sa 0 pn 1 on key {{01}} {{hex_key}}`

- Add a receive channel for a peer:

`sudo ip macsec add {{macsec0}} rx port 1 address {{52:54:00:12:34:56}}`

- Add a receive security association for a peer:

`sudo ip macsec add {{macsec0}} rx port 1 address {{52:54:00:12:34:56}} sa 0 pn 1 on key {{02}} {{hex_key}}`

- Delete a receive channel:

`sudo ip macsec del {{macsec0}} rx port 1 address {{52:54:00:12:34:56}}`

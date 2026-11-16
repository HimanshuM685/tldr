# ip ioam

> Manage IPv6 In-situ OAM (IOAM) namespaces and schemas, used to record telemetry data in packets.
> More information: <https://manned.org/ip-ioam>.

- Show all IOAM namespaces:

`ip ioam namespace show`

- Add an IOAM namespace with specific data:

`sudo ip ioam namespace add {{123}} data {{0xdeadbeef}}`

- Show all IOAM schemas:

`ip ioam schema show`

- Add an IOAM schema with specific data:

`sudo ip ioam schema add {{777}} "{{data}}"`

- Assign a schema to a namespace:

`sudo ip ioam namespace set {{123}} schema {{777}}`

- Delete an IOAM namespace:

`sudo ip ioam namespace del {{123}}`

# arpd

> Collect ARP information in a database to reduce ARP traffic on large networks.
> More information: <https://manned.org/arpd>.

- Start the daemon on a specific interface:

`sudo arpd {{eth0}}`

- Start the daemon using a specific database file:

`sudo arpd -b {{path/to/database}} {{eth0}}`

- Start the daemon and suppress ARP broadcasts sent by the kernel:

`sudo arpd -k {{eth0}}`

- Start the daemon with a specific number of active ARP probes before falling back to the kernel:

`sudo arpd -a {{3}} {{eth0}}`

- Display the contents of the database and exit:

`sudo arpd -l`

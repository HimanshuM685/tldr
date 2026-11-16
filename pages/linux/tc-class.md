# tc class

> Manage traffic control classes, which divide the traffic of a classful queueing discipline.
> See also: `tc`, `tc qdisc`, `tc filter`.
> More information: <https://manned.org/tc>.

- Show the classes of an interface:

`tc class show dev {{eth0}}`

- Show the classes of an interface with statistics:

`tc {{[-s|-statistics]}} class show dev {{eth0}}`

- Add a class with a rate limit under an HTB queueing discipline:

`sudo tc class add dev {{eth0}} parent {{1:}} classid {{1:10}} htb rate {{10mbit}}`

- Add a class with a guaranteed rate that can borrow bandwidth up to a ceiling:

`sudo tc class add dev {{eth0}} parent {{1:}} classid {{1:20}} htb rate {{5mbit}} ceil {{20mbit}}`

- Change the rate limit of an existing class:

`sudo tc class change dev {{eth0}} parent {{1:}} classid {{1:10}} htb rate {{20mbit}}`

- Delete a class:

`sudo tc class del dev {{eth0}} classid {{1:10}}`

# rtacct

> Display route realm counters, used for accounting traffic per routing realm.
> See also: `nstat`.
> More information: <https://manned.org/rtacct>.

- Display realm counters that changed since the last run:

`rtacct`

- Display counters of specific realms:

`rtacct {{realm1 realm2 ...}}`

- Display [a]bsolute counter values instead of changes since the last run:

`rtacct -a`

- Display counters including those that are [z]ero:

`rtacct -z`

- [r]eset the counter history:

`rtacct -r`

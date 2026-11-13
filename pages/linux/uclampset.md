# uclampset

> Manipulate the utilization clamping attributes of the system or a process.
> See also: `chrt`, `taskset`.
> More information: <https://manned.org/uclampset>.

- Display the utilization clamping attributes of a process:

`uclampset {{[-p|--pid]}} {{process_id}}`

- Display the utilization clamping attributes of all threads of a process:

`uclampset {{[-a|--all-tasks]}} {{[-p|--pid]}} {{process_id}}`

- Run a command with a [m]inimum and [M]aximum utilization clamp (values range from 0 to 1024):

`uclampset -m {{256}} -M {{768}} {{command}}`

- Set the [m]inimum utilization clamp of a running process:

`uclampset -m {{512}} {{[-p|--pid]}} {{process_id}}`

- Display the system-wide utilization clamping attributes:

`uclampset {{[-s|--system]}}`

- Display the maximum valid utilization clamp value:

`uclampset --max-value`

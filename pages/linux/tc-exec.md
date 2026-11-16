# tc exec

> Run traffic control helper tasks, such as debugging and updating eBPF programs.
> See also: `tc`.
> More information: <https://manned.org/tc-bpf>.

- Print the output of eBPF programs that use the trace pipe:

`sudo tc exec bpf dbg`

- Replace an eBPF program in a pinned program array map (tail call graft):

`sudo tc exec bpf graft {{path/to/pinned_map}} key {{0}} obj {{path/to/program.o}} sec {{section}}`

- Display help for eBPF tasks:

`tc exec bpf help`

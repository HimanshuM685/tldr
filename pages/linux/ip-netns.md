# ip netns

> Manage network namespaces, which give processes separate network stacks.
> More information: <https://manned.org/ip-netns>.

- List all named network namespaces:

`ip netns list`

- Create a network namespace:

`sudo ip netns add {{name}}`

- Run a command inside a network namespace:

`sudo ip netns exec {{name}} {{command}}`

- Move a network interface into a network namespace:

`sudo ip link set dev {{eth0}} netns {{name}}`

- Display the network namespace of a process:

`ip netns identify {{process_id}}`

- List the processes running in a network namespace:

`ip netns pids {{name}}`

- Delete a network namespace:

`sudo ip netns delete {{name}}`

- Monitor the creation and deletion of network namespaces:

`ip netns monitor`

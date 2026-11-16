# vdpa

> Manage vDPA (virtio data path acceleration) devices.
> More information: <https://manned.org/vdpa>.

- List the management devices that can create vDPA devices:

`vdpa mgmtdev show`

- List all vDPA devices:

`vdpa dev show`

- Create a vDPA device using a specific management device:

`sudo vdpa dev add name {{vdpa0}} mgmtdev {{vdpasim_net}}`

- Show the configuration of a vDPA device:

`vdpa dev config show {{vdpa0}}`

- Delete a vDPA device:

`sudo vdpa dev del {{vdpa0}}`

- List all vDPA devices in pretty-printed JSON format:

`vdpa {{[-j|-json]}} {{[-p|-pretty]}} dev show`

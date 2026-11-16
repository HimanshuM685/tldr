# tc action

> Manage traffic control actions independently of filters, so that they can be shared between filters.
> See also: `tc filter`.
> More information: <https://manned.org/tc-actions>.

- List all actions of a specific type:

`tc action list action {{gact|mirred|police|...}}`

- Add a generic action that passes packets, with a specific index:

`sudo tc action add action pass index {{1}}`

- Display a specific action:

`tc action get action gact index {{1}}`

- Delete a specific action:

`sudo tc action delete action gact index {{1}}`

- Delete all actions of a specific type:

`sudo tc action flush action {{gact}}`

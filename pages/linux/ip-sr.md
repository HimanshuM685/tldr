# ip sr

> Manage IPv6 Segment Routing (SRv6) settings.
> More information: <https://manned.org/ip-sr>.

- Show the source address used for SRv6 encapsulation:

`ip sr tunsrc show`

- Set the source address used for SRv6 encapsulation:

`sudo ip sr tunsrc set {{2001:db8::1}}`

- Show all SRv6 HMAC keys:

`ip sr hmac show`

- Set an HMAC key (prompts for the secret):

`sudo ip sr hmac set {{key_id}} {{sha1|sha256}}`

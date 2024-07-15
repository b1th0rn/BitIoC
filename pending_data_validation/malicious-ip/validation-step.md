There are some addresses that must always be excluded (e.g. RFC1918, multicast, loopback...)
I would always check for Martian addresses (see [RFC1812](https://datatracker.ietf.org/doc/html/rfc1812#section-5.3.7). A hit on martian address should be notified to verify the goodness of the source.

There are some wide-known good addresses (e.g. Umbrella, Cloudflare, Office365...). A hit on wide-known good addresses should be notified to verify the goodness of the source.

There could be potential grey-sources (e.g. CDN). Those should be excluded but notified. The impact could be worse if IP addresses are blacklisted. Another way is to insert a risk score which explain the impact of blocking and non blocking actions.

Specific IP:

- TOR exit nodes (which could hide behind NTP servers)
- Legit scanners (eg. Shodan)

Specific IP should be listed on dedicated lists. Specific IP should not be present on other lists.

Custom IP: we should define a format to define whitelisted IP so users can replicate the verification process.

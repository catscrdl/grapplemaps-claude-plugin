# GrappleMaps for Claude

Find Brazilian jiu-jitsu and grappling gyms, compare public listing details, and check class schedules, from a conversation with Claude. Data comes from [GrappleMaps](https://grapple-maps.com).

## Use it

Install the plugin, connect the GrappleMaps connector from the plugin's **Connectors** tab, then ask things like:

- "Find BJJ gyms near Austin, Texas that offer no-gi classes on Monday."
- "Find grappling gyms within 10 km of 30.2672, -97.7431."
- "Show the weekly schedule for the first gym."

The plugin includes the `find-gyms` skill, which tells Claude how to combine the connector's tools:

| Tool | Purpose |
| --- | --- |
| `search_gyms` | Gyms near an address or coordinates, filtered by class type, day, price, schedule availability, and radius (nearest first, up to ten) |
| `get_gym` | Public details for one gym |
| `get_gym_schedule` | A gym's weekly class schedule |

All tools are read-only. The plugin cannot post reviews, change listings, or access account data.

## Data

The plugin sends your search terms (such as a city, address, or coordinates, and any class, day, or price filters) and the gym identifiers you ask about to the GrappleMaps server at `mcp.grapple-maps.com`, which returns public gym listings and schedules. It does not store anything on your device and needs no sign-in. See the [privacy policy](https://grapple-maps.com/privacy) and [terms](https://grapple-maps.com/terms).

## Support

[grapple-maps.com/contact](https://grapple-maps.com/contact)

## License

MIT, see [LICENSE](LICENSE). This license covers the contents of this repository only, not GrappleMaps data or the GrappleMaps service.

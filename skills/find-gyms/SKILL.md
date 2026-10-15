---
name: find-gyms
description: Find Brazilian jiu-jitsu (BJJ) and grappling gyms and their class schedules. Use when the user asks for BJJ, jiu-jitsu, grappling, gi or no-gi gyms or classes near a place, wants details for a specific gym, or wants to know when a gym holds classes.
---

Use the GrappleMaps connector's read-only tools to answer questions about public gym listings.

1. **Find gyms** with `search_gyms`. Pass an `address` (city or street address) or `latitude`/`longitude`. Narrow results with `class_types` (for example gi or no-gi), `days`, `max_price` with `price_currency`, `has_schedule`, and `radius_km`. Results are nearest first, at most ten.
2. **Get details** for a gym from the results with `get_gym`, passing the `short_name` the search returned.
3. **Get the weekly schedule** with `get_gym_schedule`, passing the same `short_name`.

Guidelines:

- If the user gives no location, ask for a city or address. Never guess a default city.
- Most gyms don't list a price. When a price is missing, say it isn't listed. Never describe it as free.
- Only report days, times, and class names the tools return. Don't fill in missing details.
- Include the GrappleMaps link from each result so the user can see the full listing.
- The tools only read public listings. Decline requests to add reviews, edit listings, or look up other users' account data, and say what the connector can do instead.

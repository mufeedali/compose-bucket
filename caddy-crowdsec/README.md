# Caddy with Crowdsec

A reverse proxy solution. Adds in Crowdsec for some security.

Configured with the Cloudflare module as well for quick and easy SSL certs.

Please note that Crowdsec needs additional steps to setup.

## Environment Variables

### Required
- `TZ`: Timezone for services (e.g., `UTC`, `Asia/Kolkata`)
  - Defaults to `UTC` if not specified
  - Follow [TZ database naming](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones)

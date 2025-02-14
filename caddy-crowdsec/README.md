# Caddy with Crowdsec

A reverse proxy solution. Adds in Crowdsec for some security.

Configured with the Cloudflare module as well for quick and easy SSL certs.

Please note that Crowdsec needs additional steps to setup.

## Environment Variables

### Required
- `TZ`: Timezone for services (e.g., `UTC`, `Asia/Kolkata`)
  - Defaults to `UTC` if not specified
  - Follow [TZ database naming](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones)

## Crowdsec Bouncer Setup on First Run

Find more up-to-date information here: https://github.com/hslatman/caddy-crowdsec-bouncer

```bash
# run CrowdSec container
$ docker compose up -d crowdsec

# add the Caddy bouncer, generating an API key
$ docker compose exec crowdsec cscli bouncers add caddy-bouncer

# set the API key in your .env file as CADDY_CROWDSEC_API_KEY
$ nano .env

# run Caddy
$ docker compose up -d caddy
```

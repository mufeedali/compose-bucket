# Vaultwarden

Lightweight backend server alternative for Bitwarden. Usable with the official Bitwarden clients.

NOTE: rclone backups need additional setup. Refer to https://github.com/ttionya/vaultwarden-backup

Variables are a bit inconsistent in my setup for this one, split weirdly between environment variables and secrets. Plan to fix it one day.

## Environment Variables

### Basic

- `VAULTWARDEN_DOMAIN`: The domain or subdomain at which you plan to host the service. Format example: `https://vaultwardne.example.com`

### E-Mail Config

- `VAULTWARDEN_SMTP_FROM`: From address for the e-mails. Format-example: `sender@example.com`

### Backups

- `BACKSIES_TZ`: Timezone (e.g., `UTC`, `Asia/Kolkata`)
    - Follow [TZ database naming](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones)
- `BACKSIES_PING_URL`: Ping URL, can be used to monitor if the backup process is successful or not. Usable with Uptime Kuma, Healthchecks, etc.
- `BACKSIES_PASSWORD`: The password for the backups.
- `BACKSIES_REMOTE_DIR`: The remote directory to which to upload to.

Refer to [ttionya/vaultwarden-backup](https://github.com/ttionya/vaultwarden-backup) for futher details regarding backups.

## Secrets

I have the following files at `container-secrets/` within this directory (where the README is):

### Basic

- `vaultwarden-admin-token`: Admin token for the Vaultwarden admin web interface.

### E-Mail Config

- `vaultwarden-smtp-host`: SMTP Hostname for your provider. Mailgrid, SES, etc are examples and they will give you the host. Format example: `smtp.example.com`.
- `vaultwarden-smtp-username`: SMTP username from the provider
- `vaultwarden-smtp-password`: SMTP password from the provider

### Mobile Notifications

Required for sync to work as expected. Refer to: https://github.com/dani-garcia/vaultwarden/wiki/Enabling-Mobile-Client-push-notification

- `vaultwarden-push-id`
- `vaultwarden-push-key`

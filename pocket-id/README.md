# Pocket ID

Pocket ID is a simple and easy-to-use OIDC provider that allows users to authenticate with their passkeys to your services.

## Environment Variables

### Required Variables
- `PUID`: User ID for container permissions (default: 1000)
- `GUID`: Group ID for container permissions (default: 1000)
- `POCKET_PUBLIC_APP_URL`: The URL where users can access the application.
- `POCKET_MAXMIND_LICENSE_KEY`: API key for MaxMind's GeoIP2 service, used for determining user location based on IP address.

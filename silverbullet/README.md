# SilverBullet

SilverBullet is a note-taking application. It's kind of insane, so read more about it at the official site: [SilverBullet.md](https://silverbullet.md/).

You can find my style sheet and other config [here](https://github.com/mufeedali/silverbullet-config).

## Environment Variables

### Required Variables

- `PUID`: User ID for container permissions (default: 1000)
- `GUID`: Group ID for container permissions (default: 1000)
- `SB_USER`: Sets single-user credentials, e.g. `SB_USER=pete:1234` allows you to login with username “pete” and password “1234”.
- `SB_AUTH_TOKEN`: Enables authentication for the API. Set to any string you want, ideally a really long one. This allows you to use [the Clipper extension](https://github.com/davecburke/silverbullet-clipper).

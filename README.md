# Greite's Unraid Templates

Community Applications templates for Docker apps I maintain. One repo, multiple apps — submitted once to Unraid's Community Applications.

## Available templates

| App | Description | Image |
| --- | --- | --- |
| [speedtest-monitor](./speedtest-monitor/speedtest-monitor.xml) | Self-hosted internet speed monitor with live dashboard, history, alerts, and OIDC auth | `ghcr.io/greite/speedtest-monitor:latest` |
| [database-backup](./database-backup/database-backup.xml) | Automated PostgreSQL / MariaDB / MySQL / MongoDB dumps via cron, with rotation and healthcheck | `ghcr.io/greite/database-backup:latest` |

## Install via Community Applications

Once this repo is listed on Unraid CA, search for the app name directly in the **Apps** tab of your Unraid UI.

To pre-list the repo manually (e.g. before official listing):

1. Open **Apps → Settings → Additional search results**.
2. Paste this repo URL: `https://github.com/Greite/unraid-templates`.

## Install a single template directly

Each app exposes a `TemplateURL` pointing back to this repo, so you can also point Unraid's **Add Container** form at the raw XML:

- Speedtest Monitor: `https://raw.githubusercontent.com/Greite/unraid-templates/main/speedtest-monitor/speedtest-monitor.xml`
- Database Backup: `https://raw.githubusercontent.com/Greite/unraid-templates/main/database-backup/database-backup.xml`

## Repository layout

```
unraid-templates/
├── ca_profile.xml          # Repo-level Community Applications profile
├── README.md
├── speedtest-monitor/
│   └── speedtest-monitor.xml
└── database-backup/
    └── database-backup.xml
```

Each app lives in its own folder so we can drop in assets (icons, screenshots, app-specific notes) without polluting the root.

## Adding a new app

1. Create `unraid-templates/<app-name>/`.
2. Drop the `<app-name>.xml` Container template inside.
3. Set its `<TemplateURL>` to `https://raw.githubusercontent.com/Greite/unraid-templates/main/<app-name>/<app-name>.xml`.
4. Add a row to the table above.
5. Commit and push — CA picks the new template up automatically.

## License

MIT.

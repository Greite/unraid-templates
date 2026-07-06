# GreiteTurtle's Unraid Templates

Community Applications templates for Docker apps I maintain. One repo, multiple apps - submitted once to Unraid's Community Applications.

## Available templates

| App | Description | Image |
| --- | --- | --- |
| [speedtest-monitor](./speedtest-monitor/speedtest-monitor.xml) | Self-hosted internet speed monitor with live dashboard, history, alerts, and OIDC auth | `ghcr.io/greite/speedtest-monitor:latest` |
| [database-backup](./database-backup/database-backup.xml) | Automated PostgreSQL / MariaDB / MySQL / MongoDB dumps via cron, with rotation and healthcheck | `ghcr.io/greite/database-backup:latest` |
| [btop](./btop/btop.xml) | Unraid plugin: btop CLI + dashboard tile (top processes, load, CPU temp) | plugin (`btop.plg`) |

## Install via Community Applications

Once this repo is listed on Unraid CA, search for the app name directly in the **Apps** tab of your Unraid UI.

To pre-list the repo manually (e.g. before official listing):

1. Open **Apps → Settings → Additional search results**.
2. Paste this repo URL: `https://github.com/Greite/unraid-templates`.

## Install a single template directly

Each app exposes a `TemplateURL` pointing back to this repo, so you can also point Unraid's **Add Container** form at the raw XML:

- Speedtest Monitor: `https://raw.githubusercontent.com/Greite/unraid-templates/main/speedtest-monitor/speedtest-monitor.xml`
- Database Backup: `https://raw.githubusercontent.com/Greite/unraid-templates/main/database-backup/database-backup.xml`

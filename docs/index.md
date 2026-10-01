# Homelab Logs Dashboard

A Grafana Loki dashboard for log rates, recent messages and manual review of failure clues across homelab hosts.

## Key features

- Recent Loki log stream view.
- Log rates grouped by source and host.
- Environment and host selectors.
- Broad failure clue search for manual review.

## Quick start

Open Grafana and import `dashboards/homelab-logs.json` through **Dashboards → New → Import**. Select the configured data source and match the dashboard variables to your labels. See [Getting started](getting-started.md) for prerequisites and setup.

## Where to next

<div class="wt-grid" markdown>

[:material-rocket-launch: **Getting started**<br>Set up the required integrations](getting-started.md){ .wt-card }

[:material-download: **Installation**<br>Install and connect the required services](installation.md){ .wt-card }

[:material-tune: **Configuration**<br>Review scrape examples and dashboard variables](configuration.md){ .wt-card }

[:material-sitemap: **Architecture**<br>Follow metrics from source to dashboard](architecture.md){ .wt-card }

[:material-view-dashboard: **Dashboard usage**<br>Import and use the dashboard](usage.md){ .wt-card }

</div>

## Support

{{ support() }}

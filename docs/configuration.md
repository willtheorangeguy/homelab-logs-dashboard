# Configuration

## Precedence

This repository combines dashboard defaults with settings for external services. It defines no shared command-line, environment variable and configuration-file override order; each external service resolves its own settings.

## Integration settings

The dashboard defaults environment to homelab. The host variable queries Loki for host labels within that environment. Its log rate panels group by source and host. Supply these labels during log ingestion; this repository does not ship a collector or scrape configuration.

## Dashboard variables

| Option | Type | Default | Description |
| --- | --- | --- | --- |
| `homelab-logs.json / loki_ds` | datasource | `loki` | Grafana data source selected by the dashboard. |
| `homelab-logs.json / environment` | textbox | `homelab` | Dashboard variable whose value selects a scrape job, instance or endpoint. |
| `homelab-logs.json / host` | query | `host` | Queries the data source for available values. |

## Examples

The dashboard defaults and queries are recorded in [`dashboards/`](https://github.com/willtheorangeguy/homelab-logs-dashboard/tree/HEAD/dashboards). Import the matching JSON file in Grafana to use them.

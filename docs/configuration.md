# homelab-logs-dashboard — Configuration

The dashboard defaults environment to homelab. The host variable queries Loki for host labels within that environment. Its log rate panels group by source and host. Supply these labels during log ingestion; this repository does not ship a collector or scrape configuration.

## Dashboard variables

| Dashboard | Variable | Type | Default or query |
|---|---|---|---|
| `homelab-logs.json` | `loki_ds` | datasource | `loki` |
| `homelab-logs.json` | `environment` | textbox | `homelab` |
| `homelab-logs.json` | `host` | query | `host` |

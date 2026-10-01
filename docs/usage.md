# homelab-logs-dashboard — Dashboard Usage

Import the JSON files using **Grafana → Dashboards → New → Import**. Set the data source and variables listed in [configuration](./configuration.md).

## Homelab Logs

Source: [homelab-logs.json](../dashboards/homelab-logs.json). Refresh: `30s`.

<!-- Screenshot: after adding homelab-logs.png to .github/icons/homelab-logs-dashboard/, replace this comment with ![Homelab Logs](https://raw.githubusercontent.com/willtheorangeguy/.github/main/icons/homelab-logs-dashboard/homelab-logs.png). -->

### Panels

| Panel | Type | What it shows |
|---|---|---|
| Log rate by source | timeseries | Journal, Docker, and Alpine syslog lines per second for the selected hosts. |
| Log rate by host | timeseries | Use this to identify hosts with unusually high or missing log volume. |
| Recent logs | logs | See the query reference below. |
| Failure clues for manual review | logs | A broad text filter for investigation, not an alert or reliable error count. |

<!-- Screenshot: add a focused panel or section image here after uploading it to .github/icons/homelab-logs-dashboard/. -->

### Reading the results

The failure clues panel is a broad text search for failed, panic, fatal and i/o error. It is intended for manual review, not a reliable count or alert.

### Query reference

These expressions are copied from the dashboard JSON. Grafana substitutes the dashboard variables at runtime.

#### Log rate by source

```logql
sum by (source) (rate({environment="$environment",host=~"$host"}[5m]))
```

#### Log rate by host

```logql
sum by (host) (rate({environment="$environment",host=~"$host"}[5m]))
```

#### Recent logs

```logql
{environment="$environment",host=~"$host"}
```

#### Failure clues for manual review

```logql
{environment="$environment",host=~"$host"} |~ "(?i)(failed|panic|fatal|i/o error)"
```

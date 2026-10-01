# homelab-logs-dashboard — Troubleshooting

| Symptom | Check |
|---|---|
| No hosts in selector | query Loki for streams with the chosen environment label and a host label. |
| Empty source chart | ensure source is attached at ingestion. |
| Logs visible but no rate | widen the time range beyond the five-minute rate window. |

## First checks

Check the selected Grafana data source and dashboard variables in [configuration](./configuration.md). For Loki, inspect the labels on the ingested streams in Grafana Explore.

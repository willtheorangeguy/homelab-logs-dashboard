# homelab-logs-dashboard — Architecture

Existing log shipper -> Loki streams with environment, host and source labels -> Grafana LogQL panels.

## Components

- [dashboards/](../dashboards): Grafana dashboard definitions

## Data interpretation

The failure clues panel is a broad text search for failed, panic, fatal and i/o error. It is intended for manual review, not a reliable count or alert.

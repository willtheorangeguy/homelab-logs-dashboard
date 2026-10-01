# homelab-logs-dashboard — Installation

## Requirements

Grafana with a Loki data source and Loki streams labeled environment, host and source.

## Procedure

Import dashboards/homelab-logs.json in Grafana. Choose the Loki data source and set environment to the label value used by your streams; choose one or all hosts.

This repository contains a dashboard JSON file; it does not install or configure your Loki ingestion pipeline.

Next, review [configuration](./configuration.md) and [dashboard usage](./usage.md).

# homelab-logs-dashboard — Quickstart

## Prerequisites

Grafana with a Loki data source and Loki streams labeled environment, host and source.

## Set up

Import dashboards/homelab-logs.json in Grafana. Choose the Loki data source and set environment to the label value used by your streams; choose one or all hosts.

This dashboard reads Loki streams directly through Grafana; it has no Prometheus scrape jobs.

## Confirm data

In Grafana Explore, query Loki with the environment and host labels used by the dashboard.
For missing data, see [troubleshooting](./troubleshooting.md).

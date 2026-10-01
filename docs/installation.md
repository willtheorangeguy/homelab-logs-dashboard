# Installation

## Requirements

Grafana with a Loki data source and Loki streams labeled environment, host and source.

## Procedure

Import dashboards/homelab-logs.json in Grafana. Choose the Loki data source and set environment to the label value used by your streams; choose one or all hosts.

This repository contains a dashboard JSON file; it does not install or configure your Loki ingestion pipeline.

Next, review [configuration](configuration.md) and [dashboard usage](usage.md).

## Verify the installation

In Grafana Explore, query Loki using the `environment`, `host` and `source` labels. Then import the dashboard and confirm the selected time range contains log entries.

## Upgrading

Update the dashboard JSON from this repository when you adopt a newer version. Update any exporter or monitored service using that project's upgrade instructions.

## Uninstalling

Remove the dashboard from Grafana and remove only the scrape or deployment entries you added for this project. Keep shared monitoring services that other dashboards use.

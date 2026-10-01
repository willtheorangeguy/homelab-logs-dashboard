# Loki homelab logs dashboard

Portable monitoring bundle with example configuration. Replace example addresses and token paths for your installation; no live credentials are included.

## Requirements

Loki log streams with host and source labels.

## Dashboards

- `dashboards/homelab-logs.json`

Import the JSON in Grafana using **Dashboards > New > Import**. Select your data source from the dashboard variable(s) at the top. Update the Prometheus job variables to match your `scrape_configs` job names; use the Instance selector when present. The dashboard's JSON is also suitable for file provisioning after you have selected or provisioned data source UIDs.

Expected default job labels:

- `homelab-logs.json`: no Prometheus jobs

## Monitoring code

See the code and example configuration in this folder, if present. Keep API keys and metrics bearer tokens in local secret files or another secret manager; never commit them. Scrape examples use documentation addresses and must be edited for your network.

## Before publishing

Test against the application and Grafana versions you intend to support. Add a license you choose and check attribution for upstream components. No release or Grafana catalog upload has been performed.

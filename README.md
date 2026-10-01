<h1 align="center">homelab-logs-dashboard</h1>
<h4 align="center">A Grafana Loki dashboard for log rates, recent messages and manual review of failure clues across homelab hosts.</h4>

<div align="center">
  <img alt="GitHub Issues" src="https://img.shields.io/github/issues/willtheorangeguy/homelab-logs-dashboard">
  <img alt="GitHub Pull Requests" src="https://img.shields.io/github/issues-pr/willtheorangeguy/homelab-logs-dashboard">
  <img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-blue">
  <img alt="gitleaks workflow" src="https://github.com/willtheorangeguy/homelab-logs-dashboard/actions/workflows/gitleaks.yml/badge.svg">
  <img alt="testing workflow" src="https://github.com/willtheorangeguy/homelab-logs-dashboard/actions/workflows/testing.yml/badge.svg">
</div>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#installation">Installation</a> •
  <a href="#usage">Usage</a> •
  <a href="#documentation">Documentation</a> •
  <a href="#support">Support</a> •
  <a href="#contributing">Contributing</a> •
  <a href="#license">License</a>
</p>

<!-- Screenshot: after adding homelab-logs-dashboard/overview.png to .github/icons/, replace this comment with ![Dashboard overview](https://raw.githubusercontent.com/willtheorangeguy/.github/main/icons/homelab-logs-dashboard/overview.png). -->

A Grafana Loki dashboard for log rates, recent messages and manual review of failure clues across homelab hosts.

## Key Features

- Recent Loki log stream view.
- Log rates grouped by source and host.
- Environment and host selectors.
- Broad failure clue search for manual review.

## Installation

Grafana with a Loki data source and Loki streams labeled environment, host and source. Import dashboards/homelab-logs.json in Grafana. Choose the Loki data source and set environment to the label value used by your streams; choose one or all hosts. See [installation](docs/installation.md) for more detail.

## Usage

Import [homelab-logs.json](dashboards/homelab-logs.json) in Grafana using **Dashboards → New → Import**. Choose the data source and match the dashboard variables to your monitoring labels. See [dashboard usage](docs/usage.md).

## Documentation

Full documentation lives in [docs/](docs/README.md): [Quickstart](docs/quickstart.md) · [Configuration](docs/configuration.md) · [Architecture](docs/architecture.md) · [Dashboard usage](docs/usage.md) · [Troubleshooting](docs/troubleshooting.md).

## Support

Open a [GitHub Discussion](https://github.com/willtheorangeguy/homelab-logs-dashboard/discussions/new) or file an [issue](https://github.com/willtheorangeguy/homelab-logs-dashboard/issues/new/choose).

## Contributing

Contributions welcome. See the org-wide [Contributing Guide](https://github.com/willtheorangeguy/.github/blob/main/CONTRIBUTING.md) and [Code of Conduct](https://github.com/willtheorangeguy/.github/blob/main/CODE_OF_CONDUCT.md).

## License

MIT — see [LICENSE.md](LICENSE.md).

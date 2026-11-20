# grafana-dashboards

Grafana dashboards for monitoring AWS and Kubernetes environments with Prometheus metrics. The collection includes an Nginx Ingress dashboard for traffic, request status, latency, connections, and controller activity.

## Features

- Monitor Nginx Ingress request traffic and status codes through Prometheus metrics.
- Track success percentage with a visual indicator that changes as reliability decreases.
- Inspect latency averages, percentiles, and heatmap data.
- View controller connection counts and configuration reloads.
- Filter dashboard data by namespace and ingress.

## Installation

Clone the repository and build the Go project:

```sh
git clone <repository-url> grafana-dashboards
cd grafana-dashboards
go build -o bin/grafana-dashboards .
```

To install the binary into your Go bin directory instead:

```sh
go install .
```

## Usage

Run the command with the help option to view the available arguments:

```sh
./bin/grafana-dashboards --help
```

After building, use the dashboard definitions with Grafana and a Prometheus data source that exposes the Nginx Ingress metrics required by the dashboard. Configure the dashboard variables for the namespaces and ingresses you want to inspect.

## License

This project is licensed under the MIT License. It is based on [DevOps-Nirvana/Grafana-Dashboards](https://github.com/DevOps-Nirvana/Grafana-Dashboards), and the original MIT licensing and attribution are retained.

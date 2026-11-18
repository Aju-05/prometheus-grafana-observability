# Prometheus and Grafana Observability Lab

A local monitoring stack using Docker Compose. Prometheus scrapes Node Exporter metrics, while Grafana provides a dashboard interface. An example alert rule demonstrates a basic target availability alert.

## Components
- Prometheus for metrics collection and rule evaluation
- Node Exporter for host-level metrics
- Grafana for dashboards and visualization
- Prometheus alert rule example

## Start
```bash
docker compose up -d
```

Open Prometheus at http://localhost:9090 and Grafana at http://localhost:3000. The Compose file includes demo-only local Grafana credentials; change them before sharing or exposing the service.

Stop the stack with `docker compose down`.

## Troubleshooting
- `docker compose ps` checks container state.
- `docker compose logs prometheus` shows Prometheus logs.
- In Prometheus, check Status > Targets.
- If Node Exporter is down, inspect the Compose network and container logs.

## Security
This is a local lab. Do not expose Prometheus or Grafana directly to the internet. Use strong credentials, TLS, authentication and network restrictions in any shared environment.

## Status
Configuration is committed for local use. No live monitoring endpoint or production alert delivery is claimed.

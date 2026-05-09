# Dockerized Monitoring Stack

A production-style system monitoring stack using Prometheus, Grafana, and Node Exporter — fully containerized with Docker Compose.

## Stack
- **Prometheus** — metrics collection and storage
- **Node Exporter** — exposes host system metrics (CPU, RAM, disk, network)
- **Grafana** — visualization and dashboards

## Quick Start

```bash
git clone https://github.com/abhishekms-dev/monitoring.git
cd monitoring
docker-compose up -d
```

Then open:
- Grafana → http://localhost:3000 (admin / admin123)
- Prometheus → http://localhost:9090
- Node Exporter → http://localhost:9100/metrics

## Dashboard
Import dashboard ID `1860` (Node Exporter Full) in Grafana for full system metrics.

## Architecture
Host system → Node Exporter → Prometheus (scrapes every 15s) → Grafana (visualizes)

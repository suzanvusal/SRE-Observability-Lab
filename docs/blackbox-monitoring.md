# Blackbox Monitoring & SLA Tracking

This layer implements external service monitoring using Blackbox Exporter.

## Purpose

- Measure real user experience
- Track service uptime
- Enforce SLA & SLO objectives
- Detect outages early

## Probe Types

- HTTP
- TCP
- ICMP

## SLA Query

```promql
avg_over_time(probe_success[30d]) * 100

## Architecture
Blackbox Exporter → Prometheus → Grafana → SLA Dashboards
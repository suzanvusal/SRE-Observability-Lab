# Application Instrumentation & Golden Signals

This layer implements application-level observability using OpenTelemetry and Prometheus.

## Golden Signals

- Latency
- Traffic
- Errors
- Saturation

## Architecture

App → OpenTelemetry → OTel Collector → Prometheus → Grafana

## Key Metrics

Request Rate:
```promql
sum(rate(http_server_requests_seconds_count[5m]))

# Distributed Tracing Stack

This stack provides distributed tracing for Kubernetes workloads using OpenTelemetry and Tempo.

## Architecture

App → OpenTelemetry → Collector → Tempo → Grafana

## Components

- Tempo → Trace storage
- OpenTelemetry Collector → Trace ingestion
- Instrumented sample application

## Validation

Access app:
```bash
kubectl port-forward svc/sample-app 8080:80

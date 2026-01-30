# Monitoring Stack - Prometheus & Grafana

This stack uses kube-prometheus-stack Helm chart to deploy production-grade Kubernetes monitoring.

## Components

- Prometheus → Metrics collection
- Grafana → Dashboards
- Alertmanager → Alert processing
- Node Exporter → Node metrics
- kube-state-metrics → Kubernetes object metrics

## Installation

```bash
helm install monitoring prometheus-community/kube-prometheus-stack \
  -n monitoring \
  -f kubernetes/monitoring/prometheus-values.yaml

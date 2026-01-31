# Centralized Logging Stack

This stack provides centralized log aggregation for Kubernetes workloads.

## Architecture

Pods → Fluent Bit → Loki → Grafana

## Components

- Loki → Log storage & indexing
- Fluent Bit → Log collection
- Grafana → Visualization

## Installation

```bash
helm install loki grafana/loki-stack -n logging
helm install fluent-bit grafana/fluent-bit -n logging

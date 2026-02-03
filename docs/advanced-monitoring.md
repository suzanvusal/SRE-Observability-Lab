# Advanced SRE Monitoring

This layer focuses on deep system observability using SRE principles.

## Key Focus Areas

- CPU throttling detection
- Memory pressure analysis
- Pod efficiency metrics
- Node saturation tracking
- Capacity planning visibility

## Golden Signals

- Latency
- Traffic
- Errors
- Saturation

## Example PromQL Queries

CPU Throttling:
```promql
sum(rate(container_cpu_cfs_throttled_seconds_total[5m])) by (pod)
ß
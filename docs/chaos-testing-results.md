# Chaos Engineering Validation

## Scenarios Tested

1. Pod deletion
2. CPU stress
3. Memory stress
4. Node drain

## Observations

- Kubernetes auto-healed pods within seconds
- CPU stress increased latency
- Memory stress triggered restarts
- Burn rate alerts fired correctly

## Conclusion

System demonstrates resilience and SLO-based reliability validation.

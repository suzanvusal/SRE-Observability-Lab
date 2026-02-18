# 🚀 sre-observability-lab

> Production-grade SRE Observability & Reliability Engineering Platform built on Kubernetes.

## 📌 Project Vision

This project demonstrates **real-world Site Reliability Engineering (SRE)** practices by building a full **observability, monitoring, logging, tracing, alerting, and chaos engineering platform** for Kubernetes workloads.

The goal is to simulate **production-grade reliability engineering systems** used by large-scale tech organizations.

---

## 🏗️ High-Level Architecture
                           ┌──────────────┐
                           │   Grafana    │
                           └───────┬──────┘
                                   │
   ┌────────────┐    ┌────────────┐┴┌────────────┐
   │ Prometheus │    │    Loki     ││   Tempo     │
   └─────┬──────┘    └──────┬──────┘└──────┬──────┘
         │                  │               │
   Metrics Collector   Log Pipeline     Tracing
         │                  │               │
   ┌─────▼──────────────────▼───────────────▼─────┐
   │              Kubernetes Cluster               │
   │  (microservices + infra + exporters + apps)  │
   └───────────────────┬───────────────┬───────────┘
                       │               │
              Alertmanager        Chaos + Load Tests
                       │
                   Slack Alerts
-----------------------------------------


---

## 🧰 Tech Stack

### Observability
- Prometheus
- Grafana
- Loki
- Tempo
- Fluent Bit / Promtail

### Tracing
- OpenTelemetry

### Alerting
- Alertmanager
- Slack Webhooks

### SRE Engineering
- Chaos Engineering → LitmusChaos
- Load Testing → k6
- SLO / SLA Dashboards
- Incident Runbooks

### Infrastructure
- Kubernetes (EKS / Kind)
- Helm
- Terraform

---

## 🗂️ Repository Structure

sre-observability-lab/
├── README.md
├── architecture/
│   ├── diagrams
│   └── flows
├── terraform/
│   ├── eks
│   └── monitoring-infra
├── kubernetes/
│   ├── apps
│   ├── monitoring
│   ├── logging
│   ├── tracing
│   └── alerting
├── helm/
├── chaos/
├── load-testing/
├── dashboards/
├── alerts/
├── runbooks/
├── docs/
└── scripts/
----------------------------------
sre-observability-lab/
├── architecture/ # Diagrams & workflows
├── terraform/ # Infra provisioning
├── kubernetes/ # Kubernetes manifests
├── helm/ # Helm charts
├── chaos/ # Chaos engineering experiments
├── load-testing/ # Performance & stress tests
├── dashboards/ # Grafana dashboards
├── alerts/ # Alert rules
├── runbooks/ # Incident response playbooks
├── docs/ # Technical documentation
└── scripts/ # Automation scripts
----------------------------------

---

## 🎯 Key Goals

- Build production-grade observability stack
- Implement distributed tracing
- Design alerting & escalation pipelines
- Implement SLO-based monitoring
- Perform chaos engineering experiments
- Validate system resilience
- Build incident response playbooks

---

## 🛠️ Implementation Roadmap

- Phase 1 → Infrastructure + Base Observability
- Phase 2 → Production Monitoring + Logging + Tracing
- Phase 3 → SRE Engineering (Chaos + Load + Resilience)
- Phase 4 → Enterprise polish + documentation

---

Prometheus → Metrics  ┐
Loki → Logs           ├─→ Grafana → Correlation → Root Cause
Tempo → Traces        ┘

----
SLOs, Error Budgets & Burn Rate Monitoring (Elite SRE Level)
🎯 Objectives

You will implement:

Service Level Objectives (SLOs)

Error Budget tracking

Burn rate alerting using Prometheus + Alertmanager

Real-world SRE alert strategy used by Google, Meta, Uber, Stripe

sre-observability-lab/
├── slo/
│   ├── latency-slo.yaml
│   ├── availability-slo.yaml
│   └── burnrate-alerts.yaml


---------
Can your system survive failure?

We will:

Inject failures intentionally

Validate Kubernetes self-healing

Observe metrics + alerts triggering

Prove SLO burn rate behavior under chaos


## 👨‍💻 Author

**Sujan Bhusal**  
Cloud & DevOps Engineer  
Toronto, Canada  

---

## ⭐ If you find this project useful, consider starring the repo!

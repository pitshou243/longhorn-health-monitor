# longhorn-health-monitor

## Overview

The Longhorn Health Monitor provides proactive alerting for Longhorn storage health using Prometheus and Rancher Monitoring.

The monitor focuses on:

- Volume Health
- Replica Health
- Engine Health
- Node Health
- Disk Health
- Capacity Monitoring
- Metrics Availability

This project intentionally does **not** monitor Longhorn backups.

For backup monitoring, see:

https://github.com/pitshou243/longhorn-backup-silent-failure-alerter

---

## Features

- PrometheusRule alerts
- Rancher Monitoring compatible
- Grafana dashboard
- Runbook documentation
- Metric validation guide

---

## Installation

```bash
kubectl apply -f deploy/longhorn-health-rules.yaml
```

---

## Documentation

| Document | Description |
|----------|-------------|
| docs/metric-validation.md | Verify Longhorn metrics |
| docs/alert-reference.md | Complete alert descriptions |
| docs/runbook.md | Troubleshooting guide |

---

## Repository Layout

```text
deploy/
dashboards/
docs/
examples/
```

---

## License

Apache-2.0

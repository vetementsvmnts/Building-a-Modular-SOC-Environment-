# Building a Modular SOC Environment

 Enterprise-grade Security Operations Center (SOC) featuring automated threat detection, SIEM correlation, EDR telemetry ingestion, and custom detection engineering. Built for blue team operations, incident response workflows, and adversary simulation detection validation.

## 🎯 What This Covers

- **Centralized Log Aggregation** — Collect, parse, and normalize logs from any source
- **Real-Time Alerting** — Detection rules with automated prioritization
- **Threat Intelligence Pipelines** — IOC ingestion, enrichment, and blocking
- **Automated Incident Response** — Playbooks for containment and remediation

## 🏗️ Architecture Overview

![SOC Architecture](docs/images/soc-architecture.png)

## 📂 Repository Structure

| Module | Purpose |
|--------|---------|
| `01-Architecture/` | Diagrams, network design, infrastructure docs |
| `02-Log-Aggregation/` | Parser configs, ingestion pipelines |
| `03-Detection-Engineering/` | Detection rules mapped to MITRE ATT&CK |
| `04-Alerting-Response/` | SOAR playbooks, escalation policies |
| `05-Threat-Intelligence/` | IOC feeds, enrichment workflows |
| `06-EDR-Telemetry/` | Endpoint agent configs, deployment scripts |
| `07-Automation/` | Python, PowerShell, Terraform scripts |
| `08-Dashboards/` | Grafana, Kibana, Sentinel visualizations |
| `09-Threat-Hunting/` | Hunt hypotheses, purple team exercises |
| `10-Incident-Response/` | Runbooks, forensics procedures |
| `11-Compliance/` | Audit evidence, reporting templates |
| `12-Training/` | Labs, onboarding, certification guides |

## 🚀 Quick Start

1. **Review** the architecture in `01-Architecture/`
2. **Deploy** log collectors from `02-Log-Aggregation/`
3. **Enable** detection rules in `03-Detection-Engineering/`
4. **Configure** alerting playbooks in `04-Alerting-Response/`

## 📜 License

MIT License — See [LICENSE](LICENSE)

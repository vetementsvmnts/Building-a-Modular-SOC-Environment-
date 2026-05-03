# Building a Modular SOC Environment

&gt; **Enterprise-grade Security Operations Center (SOC) environment featuring automated threat detection, SIEM correlation, EDR telemetry ingestion, and custom detection engineering. Built for blue team operations, incident response workflows, and adversary simulation detection validation.**

---

## 🏗️ Architecture Overview



```
╔══════════════════════╗                              ╔══════════════════════╗
║     KALI LINUX       ║   ──── Simulated Attacks ──▶ ║     WINDOWS 10      ║
║     Attacker         ║   ◀─── Attack Telemetry ───  ║     Victim          ║
║   192.168.56.10      ║                              ║   192.168.56.20      ║
╚══════════╤═══════════╝                              ╚══════════╤═══════════╝
           │                                                     │
           │              Sysmon + Windows Event Logs            │
           └─────────────────────────┬───────────────────────────┘
                                     │
                                     ▼
                        ╔════════════════════════╗
                        ║      WAZUH SIEM         ║
                        ║      MANAGER            ║
                        ║    192.168.56.100       ║
                        ╚════════════╤════════════╝
                                     │
                              Log Ingestion &
                              Alert Correlation
                                     │
                                     ▼
                        ╔════════════════════════ ╗
                        ║   ANALYST DASHBOARD     ║
                        ║   Kibana  │  Grafana    ║
                        ╚════════════╤════════════╝
                                     │
                             Detection Rule
                               Enforcement
                                     │
                                     ▼
                        ╔════════════════════════╗
                        ║   CUSTOM SIGMA RULES   ║
                        ║   YARA SIGNATURES      ║
                        ║   MITRE ATT&CK MAPPED  ║
                        ╚════════════════════════╝
```


---

## 🖥️ Lab Environment

| Component | Role | IP Address | Tools |
|-----------|------|------------|-------|
| **Kali Linux** | Attacker / Purple Team | 192.168.56.10 | Nmap, Metasploit, Hydra, Scapy |
| **Windows 10** | Victim Endpoint | 192.168.56.20 | Sysmon, Wazuh Agent |
| **Ubuntu Server** | Wazuh SIEM / Log Aggregation | 192.168.56.100 | Wazuh Manager, Elasticsearch |
| **pfSense** | Network Firewall / IDS | 192.168.56.1 | Snort, Suricata |

---

## 🚀 Quick Start

### Prerequisites
- VirtualBox or VMware Workstation
- 16GB+ RAM recommended
- 100GB+ free disk space

### 1. Clone This Repository
```bash
git clone https://github.com/vetementsvmnts/Building-a-Modular-SOC-Environment-.git
cd Building-a-Modular-SOC-Environment-

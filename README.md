# Enterprise Virtual Data Center & SDDC Deployment 🏢☁️

## 📝 Project Overview
This repository showcases the architectural design and deployment phase blueprints for an enterprise-level Software-Defined Data Center (SDDC) tailored for higher education administrative and staging lab environments. 

The primary milestone was eliminating physical hardware dependencies by building an agile, scalable virtual infrastructure engineered for maximum uptime and secure multi-tenant network separation.

---

## 🏗️ 9-Phase Core Deployment Architecture
The data center engineering was executed through a rigorous 9-stage infrastructure lifecycle:

```text
┌──────────────────────────────┐
│  Phase 1 & 2: Bare-Metal     │ ──► Deployed 3x ESXi 7 U2 Hosts
│  & iSCSI NAS Storage         │ ──► Configured LUNs on shared storage
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│  Phase 3: Central Orchestration│ ──► Spun up vCenter 8 Engine
│  & Resource Pooling          │ ──► Activated vMotion, DRS, and HA Clusters
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│  Phase 4, 5 & 6: Operations, │ ──► Observability: Zabbix & PRTG
│  Security & Backup Core      │ ──► DR: Veeam Backup & Recovery
│                              │ ──► Security: Kaspersky Master Node
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│  Phase 7 & 8: Automation     │ ──► IaC: Ansible Playbooks for provisioning
│  & Educational Services      │ ──► Services: Apache Web Clusters, Postfix Mail
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│  Phase 9: Network Virtualization│ ──► Enforced Logical Network Isolation via NSX
│  & Micro-segmentation        │ ──► Deployed GNS3 Simulation Clusters

# ⚖️ Litigation War Room & Deposition IT Operations

### Service Coordination • Equipment Tracking • Credential Administration • Verified Recovery • Network Diagnostics

![Salesforce](https://img.shields.io/badge/Salesforce-Service_Management-00A1E0?style=flat-square)
![Snipe-IT](https://img.shields.io/badge/Snipe--IT-Asset_Management-2563EB?style=flat-square)
![1Password](https://img.shields.io/badge/1Password-Access_Administration-3B66BC?style=flat-square)
![Backblaze B2](https://img.shields.io/badge/Backblaze_B2-Recovery-E21E29?style=flat-square)
![QuickBooks](https://img.shields.io/badge/QuickBooks-Service_Billing-2CA01C?style=flat-square)
![macOS](https://img.shields.io/badge/macOS-Network_Diagnostics-475569?style=flat-square)

> **Organized a deposition-support workflow across service requests, equipment, access, recovery, billing, and connectivity checks — with a verified transcript restoration and documented DNS troubleshooting results.**

---

## 📌 Project at a Glance

| | |
|---|---|
| **Purpose** | Prepare and document technology readiness for a hybrid deposition |
| **Reference** | **DEPO-2026-001** · Salesforce Case **00001026** |
| **Scope** | Five asset records · Three credential records · Transcript recovery · Service invoice · Network diagnostics |
| **Coordination** | Manual updates, shared engagement references, and asset tags linking equipment, credentials, and recovery records |

---

## 🏗️ Project Workflow

### 1️⃣ Salesforce — Service Requests & Readiness Planning

- Created **Case 00001026**, assigned High priority and an owner, and recorded **DEPO-2026-001**.
- Added equipment and connectivity tasks with deadlines, readiness instructions, and escalation guidance.

```mermaid
flowchart LR
    C["📋 Salesforce<br/>Case 00001026"] --> T["Readiness tasks<br/>Equipment + connectivity"]
    C -. "Engagement reference" .-> A["💻 Snipe-IT<br/>5 asset records"]
    C -. "Engagement reference" .-> I["🧾 QuickBooks<br/>Invoice 1038"]
    classDef blue fill:#E0F2FE,stroke:#0284C7,color:#0C4A6E,stroke-width:2px;
    classDef green fill:#DCFCE7,stroke:#16A34A,color:#14532D,stroke-width:2px;
    class C,T,A blue;
    class I green;
```

Dashed connections represent manual record coordination through **DEPO-2026-001**.

<p align="center">
  <img src="evidence/01-salesforce-readiness-tasks.png" width="90%" alt="Salesforce equipment and connectivity readiness tasks referencing Case 00001026">
  <br><sub>Priority, ownership, deadlines, and escalation instructions captured in the readiness tasks.</sub>
</p>

**Next enhancement:** define SLA response and resolution targets, business hours, and escalation thresholds; track acknowledgement and service-restoration times against those targets.

### 2️⃣ Snipe-IT — Equipment Inventory & Checkout

Registered five assets and captured their checkout state, providing identifiable equipment references for the remaining phases.

| Asset tag | Equipment |
|---|---|
| LAB-LT-001 / LAB-LT-002 | Two Dell XPS 13 laptops |
| LAB-VC-001 | SoundStation 2 |
| LAB-MN-001 | UltraSharp U2415 display |
| LAB-PR-001 | Wireless access point |

<p align="center">
  <img src="evidence/02-snipe-it-inventory.png" width="90%" alt="Five Snipe-IT equipment records with Checkin actions">
  <br><sub>Asset tags, models, and checkout state preserved in the equipment register.</sub>
</p>

**Next enhancement:** add maintenance history and workstation hardening checks covering patch status, disk encryption, host firewall settings, and [Group Policy security baselines](https://learn.microsoft.com/windows/security/operating-system-security/device-management/windows-security-configuration-framework/windows-security-baselines).

### 3️⃣ 1Password — Credential Organization & Guest Access

Created the **DEPO-2026-001 — IT Operations** vault with AV console, test Wi-Fi, and backup workstation credential records. Assigned guest access and linked the workstation record to **LAB-LT-001** from the equipment inventory.

<p align="center">
  <img src="evidence/03-1password-vault.png" width="90%" alt="IT Operations vault with three credential records and concealed passwords">
  <br><sub>Equipment-related credentials organized in a dedicated engagement vault.</sub>
</p>

**Next enhancement:** verify least-privilege access, credential rotation, and offboarding. Extend Windows account administration with **Active Directory (AD) security groups** and [Windows LAPS](https://learn.microsoft.com/en-us/windows-server/identity/laps/laps-scenarios-windows-server-active-directory) for local administrator password management.

### 4️⃣ Backblaze B2 — Record Storage & Verified Recovery

Uploaded the transcript, equipment reference, and exhibit register. Restored the transcript and checked its **SHA-256 checksum** against the original.

```mermaid
flowchart LR
    S["📄 Source records"] --> B[("☁️ Backblaze B2")]
    B --> R["Downloaded<br/>transcript"]
    R --> V{"SHA-256<br/>match: OK"}
    classDef blue fill:#E0F2FE,stroke:#0284C7,color:#0C4A6E,stroke-width:2px;
    classDef violet fill:#EDE9FE,stroke:#7C3AED,color:#4C1D95,stroke-width:2px;
    classDef green fill:#DCFCE7,stroke:#16A34A,color:#14532D,stroke-width:2px;
    class S,R blue;
    class B violet;
    class V green;
```

<p align="center">
  <img src="evidence/04-restored-transcript-checksum.png" width="90%" alt="Restored transcript passes SHA-256 verification">
  <br><sub>Recovery check returned <code>deposition-transcript.txt: OK</code>.</sub>
</p>

**Next enhancement:** schedule backups, define recovery point and recovery time objectives (**RPO/RTO**), measure restore times, and alert on failed backup or integrity checks.

### 5️⃣ QuickBooks — Engagement Billing

Created **invoice 1038**, placing **DEPO-2026-001** in the service description to connect billing with the support request.

| Service description | Quantity | Rate | Before-tax amount |
|---|---:|---:|---:|
| Room setup, connectivity validation, and technical support | 3 hours | $100 | **$300** |

**Next enhancement:** track support hours and equipment expenses by engagement reference, reconcile invoice lines against approved work, and report the cost of each engagement.

### 6️⃣ macOS Networking — Diagnostics & Readiness Assessment

Used **dig**, **ping**, and **networkQuality** to measure the connection and compare DNS resolver behavior.

```mermaid
flowchart LR
    Q["🔎 DNS lookup"] --> U["192.0.2.1"]
    U --> F["⏱️ Timeout"]
    Q --> D["Normal resolver"]
    D --> P["✅ NOERROR<br/>120 ms"]
    classDef blue fill:#E0F2FE,stroke:#0284C7,color:#0C4A6E,stroke-width:2px;
    classDef red fill:#FEE2E2,stroke:#DC2626,color:#7F1D1D,stroke-width:2px;
    classDef green fill:#DCFCE7,stroke:#16A34A,color:#14532D,stroke-width:2px;
    class Q,D blue;
    class U,F red;
    class P green;
```

| Check | Recorded result |
|---|---|
| Ping to 1.1.1.1 | **10/10 replies**, **0% loss**, **115.594 ms** average |
| Download / upload | **100.424 / 74.969 Mbps** |
| Responsiveness under load | **Low — 528.296 ms** |
| Normal DNS retest | **NOERROR**, two answers, **120 ms** |

The controlled DNS test affected one query without changing system settings. Low responsiveness identified a follow-up requirement: validate conferencing under load.

<p align="center">
  <img src="evidence/05-network-diagnostics.png" width="75%" alt="Network performance measurements and DNS timeout followed by a successful retest">
  <br><sub>Recorded performance findings alongside the expected DNS failure and successful normal lookup.</sub>
</p>

**Next enhancement:** deploy the [proposed staff, guest, and AV VLAN design](network-tests/Network-Plan.md); verify **DHCP addressing, DNS resolution, firewall ACLs, and guest isolation**, then test conferencing under load.

---

## ✅ Key Outcomes

- **Traceable operational records:** shared engagement reference across service coordination, credential organization, recovery documentation, and invoicing.
- **Verified file recovery:** restored transcript matched the original SHA-256 checksum.
- **Evidence-based network assessment:** captured successful connectivity and DNS results while identifying low responsiveness requiring further validation.

---

## 💡 Skills Developed

### 📋 Service Management & Documentation

- [x] Prioritized support requests, assigned ownership, and documented readiness deadlines.
- [x] Recorded escalation guidance and maintained engagement traceability.
- [x] Prepared service invoice details and organized supporting evidence.

### 💻 Equipment & Access Administration

- [x] Registered equipment and tracked checkout state through unique asset tags.
- [x] Organized equipment-related credentials in a dedicated vault.
- [x] Provisioned guest vault access and linked credential records to assets.

### 🌐 TCP/IP Networking & Troubleshooting

- [x] Compared DNS resolver behavior and documented lookup results.
- [x] Analyzed ICMP packet loss and round-trip latency.
- [x] Measured upload/download capacity and responsiveness under load.
- [x] Planned staff, guest, and AV VLAN segmentation.

### ☁️ Backup, Recovery & Integrity

- [x] Uploaded and organized recovery records in cloud storage.
- [x] Restored the transcript and verified its SHA-256 checksum.
- [x] Preserved diagnostic outputs and recovery evidence for review.

---

## 📚 Supporting Files

- [Network design](network-tests/Network-Plan.md)
- [Raw network diagnostic records](network-tests/)
- [Back to my projects portfolio](https://github.com/SaberYasser/Profile)

---

## 🤝 README Contribution

Codex assisted with drafting and refining this README, including its structure, wording, diagrams, and presentation of project evidence.

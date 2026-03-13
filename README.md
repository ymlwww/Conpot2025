# Copot-2025 Honeypot Dataset

## Overview

The **Copot-2025 dataset** contains attacker interaction data collected using the **Cowrie SSH/Telnet honeypot** from **April 15, 2025 to July 7, 2025**.  
The dataset records attacker sessions including authentication attempts, command execution, and file uploads observed during the honeypot deployment.

To enrich the dataset with threat intelligence, IP addresses and file hashes were checked primarily using **VirusTotal**, with additional information obtained from:

- AbuseIPDB
- IPInfo
- IPQualityScore

Sensitive identifiers such as IP addresses, file hashes, and session messages are **anonymized using Crypto-PAn techniques** to preserve privacy while maintaining prefix consistency for network analysis.

The dataset is **actively being updated**, and additional honeypot data will be released in future updates.

If you use this dataset, please cite our paper:

> **Copot-2025: Six-Month Observation of Honeypots**  
> IEEE International Conference on Communications Workshops (ICC Workshops), 2026

---

# Dataset Schema

Each row in the dataset represents **one attacker session interacting with the honeypot**.

| Field | Description |
|------|-------------|
| **Session ID** | Unique identifier for the attacker session within the honeypot |
| **Src IP (anonymized)** | Attacker source IP address anonymized using Crypto-PAn |
| **Src Port** | Source port used by the attacker |
| **Dst IP** | IP address of the honeypot being accessed |
| **Dst Port** | Port of the honeypot service |
| **Protocol** | Connection protocol used (e.g., SSH, Telnet) |
| **Timestamp Start** | Session start time |
| **Timestamp End** | Session end time |
| **Event Count** | Number of messages/events during the session |
| **Username(s)** | Usernames attempted during authentication |
| **Password(s)** | Passwords attempted during authentication |
| **Commands** | Commands executed during the session |
| **Uploaded Files** | Files uploaded by the attacker |
| **File Hashes (anonymized)** | Anonymized hashes of uploaded files |
| **Messages (anonymized)** | Session message logs with anonymization |
| **Threat Labels** | Threat labels aggregated from threat intelligence sources |
| **Reputation Score** | Reputation score derived from community reports |
| **Geo Location** | Geographic location inferred from attacker IP |
| **ISP** | Internet Service Provider of the attacker IP |
| **SSH Version** | SSH client version used by the attacker |
| **SSH Fingerprint** | SSH key fingerprint |
| **Malicious** | Binary label: `1` indicates malicious behavior, `0` indicates benign |

---

# Threat Intelligence Annotation

Threat intelligence information was gathered from multiple sources including:

- VirusTotal
- AbuseIPDB
- IPInfo
- IPQualityScore

Note:

> In some cases, a **threat label may appear even when the reputation score is 0**.  
> This occurs because threat labels aggregate signals from **90+ security vendors**, whereas reputation scores rely primarily on **community reports**.

---

# Malicious Label Definition

The **Malicious** field is assigned using the following heuristic:

A session is labeled as **malicious (`1`)** if:

- The attacker attempts to authenticate using the username **`root`**, OR
- The associated **reputation score > 50**

Otherwise, the session is labeled as **benign (`0`)**.

---

# Citation

If you use this dataset in your research, please cite:
@inproceedings{yu2026copot,
title={Copot-2025: Six-Month Observation of Honeypots},
author={Yu, Mingli and Davis, Parker and La Porta, Thomas and Cao, Guohong and Hemida, Ahmed H. Anwar},
booktitle={IEEE International Conference on Communications Workshops (ICC Workshops)},
year={2026},
organization={IEEE}
}


---

# Authors

- **Mingli Yu** — Pennsylvania State University  
- **Parker Davis** — Pennsylvania State University  
- **Thomas La Porta** — Pennsylvania State University  
- **Guohong Cao** — Pennsylvania State University  
- **Ahmed H. Anwar Hemida** — DEVCOM Army Research Laboratory  

---

# Conference

**2026 IEEE International Conference on Communications Workshops (ICC Workshops)**  

Workshop:  
**WS-24: Cybersecurity of Digital Twins and Interconnected Cyber Physical Systems (SecCPS)**

---

# Dataset Updates

We are **continuously expanding the Copot dataset** with additional honeypot observations.  
Future releases will include longer observation periods and additional telemetry.

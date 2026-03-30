# Log Dataset for Importance Scoring and Cross-Signalling Correlation
---
# Overview

This repository contains a synthetic log dataset generated for a log analysis system. The dataset is designed to simulate real-world logs from multiple sources and supports tasks such as log parsing, normalization, importance scoring, and incident correlation.

---
# Dataset Description

The dataset includes 10,000+ log entries in syslog-style format. Logs are generated from different system components to reflect a heterogeneous environment.

Log Types Included:
- Network logs (OSPF, PORT, VLAN)
- Security logs (port scan detection, MAC blocking, ACL errors)
- Authentication logs (SNMP failures)
- DHCP logs (DHCP snooping events)
- System logs (syslog messages)
- Configuration logs (Manager events)

Format:

Each log entry follows a syslog-style format:
- <priority>timestamp host service: message

Example:
- <191>Mar 12 10:00:25 sw-access-01 PORT: port 1/0/20 changed state to down

---

# Schema Alignment

The dataset is designed to be processed into a structured schema containing:
- sequence_number
- timestamp
- source_type
- service
- host
- log_level
- event_type
- event_action
- template_id
- frequency
- event_weight
- importance_score
- correlation_id
- message
- metadata

---

# Purpose

This dataset is intended for:
- Log parsing and normalization
- Template extraction
- Feature computation (frequency, event weight)
- Importance scoring
- Incident detection and correlation

---

# Usage

- Use the dataset as input to the log ingestion pipeline.
- Parse logs to extract structured fields.
- Apply scoring and correlation techniques.
- Visualize or analyze detected incidents.

---

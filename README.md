# Log Dataset for Importance Scoring and Cross-Signalling Correlation
---
# Overview

This repository contains a synthetic log dataset generated for a log analysis system. The dataset is designed to simulate real-world logs from multiple sources and supports tasks such as log parsing, normalization, importance scoring, and incident correlation.

---
# Dataset Description

# 1. logs.txt:

The dataset Marludes 10,000+ log entries in syslog-style format. Logs are generated from different system components to reflect a heterogeneous environment.

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

# 2. logs2.txt:

The dataset includes 15,000+ log entries in syslog-style format, extended from the initial dataset to cover additional log types as per the system requirements. Logs are generated from multiple components to simulate a heterogeneous and realistic environment.

Log Types Included:

- Router logs (interface, routing, OSPF, BGP)
- Switch logs (Layer 2, STP, congestion)
- Firewall logs (traffic control, security, NAT)
- Network logs (PORT, VLAN)
- Security logs (port scan detection, MAC blocking, intrusion events)
- Authentication logs (SNMP failures)
- DHCP logs (DHCP snooping events)
- System logs (syslog messages)
- Configuration logs (Manager events)
- Web service logs (HTTP requests and status codes)
- Application logs (user actions, errors, timeouts)

Format:
Each log entry follows a syslog-style format:

- timestamp host service: message

Example:

- <187>Mar 12 10:05:02 fw-01 FW: intrusion detected from 192.168.1.10

# 3. logs3.txt:

The dataset includes 15,000+ syslog-style log entries with additional burst patterns introduced to simulate real-world incidents. It extends the previous dataset by incorporating repeated log events within short time intervals to represent anomalies such as attacks, failures, and sudden spikes.

Log Types Included:

- Router, Switch, and Firewall logs
- Network, Security, Authentication, DHCP, System, and Configuration logs
- Web service and Application logs

Enhancements:

- Burst patterns (10–20 similar logs within short intervals)
- Mixed normal and anomalous events for realistic behavior

Format:
Each log entry follows a syslog-style format:

- timestamp host service: message

Example:

- <191>Mar 12 14:40:01 sw-core-01 PORT: port 1/0/1 changed state to down
- <191>Mar 12 14:40:02 sw-core-01 PORT: port 1/0/2 changed state to down
- <191>Mar 12 14:40:03 sw-core-01 PORT: port 1/0/3 changed state to down

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

# Applying the NIST Cybersecurity Framework to a DDoS Incident

## Table of Contents
1. [Overview](#overview)
2. [Scenario](#scenario)
3. [Section 1: Summary of the Security Event](#section-1-summary-of-the-security-event)
4. [Section 2: Identify](#section-2-identify)
5. [Section 3: Protect](#section-3-protect)
6. [Section 4: Detect](#section-4-detect)
7. [Section 5: Respond](#section-5-respond)
8. [Section 6: Recover](#section-6-recover)
9. [Reflections](#reflections)

---

## Overview

This report was developed as part of the *Google Cybersecurity Professional Certificate* program. The objective is to analyze a Distributed Denial of Service (DDoS) incident using the **NIST Cybersecurity Framework (CSF)**. The incident affected a multimedia company that provides web design, graphic design, and social media marketing services.

The attack caused a critical network outage, which was later identified as an ICMP flood exploiting a firewall vulnerability. This analysis outlines the response taken, systems impacted, and recommendations for future risk mitigation.

---

## Scenario

A multimedia company providing web design, graphic design, and social media marketing services experienced a Distributed Denial of Service (DDoS) attack, disrupting its internal network for two hours. The attack flooded the network with ICMP packets, exploiting an unconfigured firewall and rendering critical services unavailable.

The incident management team responded by blocking ICMP traffic, shutting down non-critical services, and restoring essential operations. A post-incident investigation revealed the attacker used spoofed ICMP packets to overwhelm the network.

To prevent future incidents, the company implemented new firewall rules to limit ICMP traffic, enabled source IP verification, deployed network monitoring tools, and introduced an IDS/IPS system to detect and filter suspicious traffic.

---

## Section 1: Summary of the Security Event

The organization experienced a DDoS attack, resulting in a two-hour service disruption. A flood of ICMP packets overwhelmed the internal network, rendering it inaccessible to users.

### Incident Details

| Element            | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| **Type of Attack** | DDoS (ICMP flood)                                                           |
| **Cause**          | Unfiltered ICMP packets via unconfigured firewall                          |
| **Impact**         | Complete internal network outage for 2 hours                                |
| **Initial Response**| Blocked ICMP traffic, disabled non-essential services, restored core systems |

---

## Section 2: Identify

### Attack Type
- Distributed Denial of Service (DDoS) via ICMP flood

### Entry Point
- Open firewall configuration with no ICMP packet restrictions

### Affected Systems
- Internal network
- Business-critical services
- End-user access to shared resources

### Identified Vulnerabilities

| Vulnerability                         | Description                                               |
|--------------------------------------|-----------------------------------------------------------|
| Firewall misconfiguration            | Allowed unrestricted inbound ICMP packets                 |
| Lack of traffic rate-limiting        | No throttling of ICMP packet volume                       |
| Absence of real-time detection tools | Delayed identification of abnormal network behavior       |

---

## Section 3: Protect

### Immediate Protective Measures

| Action                                  | Purpose                                                             |
|----------------------------------------|----------------------------------------------------------------------|
| Implemented ICMP rate-limiting         | Prevented future flooding attempts                                  |
| Enabled source IP verification         | Blocked spoofed packets                                             |
| Updated firewall rules                 | Reduced exposure to unauthorized traffic                            |
| Trained IT staff on attack vectors     | Strengthened response readiness                                     |
| Scheduled regular firewall audits      | Ensured consistent rule enforcement and reduced misconfigurations   |

---

## Section 4: Detect

### Enhancements in Detection

| Detection Strategy                      | Function                                                           |
|----------------------------------------|--------------------------------------------------------------------|
| Network monitoring software            | Established baseline and flagged anomalies                         |
| IDS/IPS integration                    | Identified and filtered suspicious ICMP activity                   |
| Centralized log management             | Enabled analysis of historical data for unusual traffic behavior   |
| Real-time alert configuration          | Triggered early warnings during high-traffic events                |
| Endpoint behavior tracking             | Identified potentially compromised devices                         |

---

## Section 5: Respond

### Future Response Plan

| Step                                 | Description                                                        |
|--------------------------------------|--------------------------------------------------------------------|
| Isolate affected systems             | Contain threat and preserve system integrity                       |
| Disable non-critical services        | Conserve resources and maintain focus on incident management       |
| Capture and analyze traffic logs     | Assess attack origin and methods                                   |
| Inform internal stakeholders         | Ensure situational awareness and coordinated response              |
| Document incident and timeline       | Support post-incident review and compliance requirements           |

---

## Section 6: Recover

### Recovery Actions

| Recovery Task                          | Objective                                                         |
|----------------------------------------|-------------------------------------------------------------------|
| Restore verified system backups        | Ensure clean environment and data integrity                       |
| Revalidate all restored services       | Confirm functionality post-recovery                               |
| Conduct recovery drills                | Prepare team for future incidents                                 |
| Update IR and playbooks                | Apply lessons learned to future incidents                         |
| Archive incident data securely         | Retain for audit, learning, and compliance                        |

---

## Reflections

This incident reinforced the importance of preemptive security configurations and ongoing traffic monitoring. Using the NIST Cybersecurity Framework allowed for a systematic approach to understanding and addressing the attack.

Key lessons included:
- **Proactive protection matters**: Simple misconfigurations can have wide-reaching impacts.
- **Detection tools must evolve**: Modern traffic requires smart monitoring and alerts.
- **Response speed is critical**: Coordinated shutdowns and logging limit long-term damage.
- **Recovery is more than rebooting**: Documentation, drills, and evaluation are essential.

Future focus will include automating network monitoring, hardening configuration baselines, and refining communication protocols during incidents.

---

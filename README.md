# pfBlocker-NG Deployment – pfSense Homelab Project

## Overview

This project documents the deployment and configuration of **pfBlocker-NG** on **pfSense** within my cybersecurity homelab.

The objective was to design and implement a perimeter control solution capable of:

* Blocking malicious IP addresses and domains
* Preventing access to NSFW, gambling, and social media sites
* Enforcing geographic-based IP restrictions (GeoIP filtering)
* Integrating threat intelligence feeds into firewall policy
* Generating actionable logs for monitoring and validation

This project simulates enterprise-level network defense controls using open-source technologies.

---

## Project Objectives

* Implement DNS-based filtering (DNSBL)
* Enforce IP reputation blocking
* Apply GeoIP-based access control
* Enable logging and monitoring for validation
* Demonstrate layered security at the firewall

---

## Lab Environment

* **Firewall:** pfSense
* **Package Installed:** pfBlocker-NG
* **Internal Network:** Segmented lab network with test clients
* **Logging:** Enabled for DNSBL, IPv4 filtering, and GeoIP rules
* **Testing:** Simulated malicious and restricted traffic

---

## Implementation Steps

### 1. Installation

* Installed pfBlocker-NG via pfSense Package Manager
* Verified service activation
* Enabled automatic updates

---

### 2. DNSBL Configuration (Domain Filtering)

Configured DNSBL to block:

* Malicious domains
* NSFW content
* Gambling websites
* Social media platforms

Actions performed:

* Enabled DNSBL feature
* Integrated domain blocklists
* Configured update frequency
* Enabled logging
* Verified DNS Resolver integration

Result:
Blocked domains redirected to sinkhole page and logged for monitoring.

---

### 3. IP Reputation Filtering (IPv4)

Configured IPv4 filtering to:

* Block known malicious IP ranges
* Prevent outbound traffic to threat intelligence feeds
* Prevent inbound connections from suspicious IP addresses

Actions performed:

* Enabled IPv4 filtering
* Added reputation feeds
* Applied auto-generated firewall rules
* Verified rule order and enforcement

Result:
Malicious IP traffic blocked at the perimeter and visible in firewall logs.

---

### 4. GeoIP Filtering

Implemented geographic restrictions to:

* Block inbound traffic from selected countries
* Restrict outbound connections to high-risk regions

Actions performed:

* Enabled GeoIP functionality
* Downloaded and updated GeoIP database
* Selected countries for blocking
* Applied policies to WAN and LAN rules

Result:
Geo-restricted traffic successfully denied and logged.

---

### 5. Logging & Monitoring

Enabled logging for:

* DNSBL events
* IPv4 block events
* GeoIP enforcement

Validated controls using:

* pfSense firewall logs
* pfBlocker-NG reports
* Client-side testing

---

## Testing & Validation

Simulated the following scenarios:

* Attempted access to malicious domains
* Access to gambling and NSFW sites
* Connections to blocked IP addresses
* Traffic from restricted geographic IP ranges

All enforcement policies functioned as expected.

---

## Security Outcomes

* Implemented layered defense at the network perimeter
* Reduced exposure to malicious infrastructure
* Enforced acceptable use policy controls
* Integrated automated threat intelligence feeds
* Demonstrated firewall rule analysis and validation

---

## Skills Demonstrated

* Firewall hardening
* DNS-based security enforcement
* IP reputation filtering
* GeoIP policy enforcement
* Log analysis and validation
* Threat intelligence integration
* Independent research and documentation

---

## Demonstration

A recorded video demonstration is available showing:

* Live testing
* Log validation

---

## Why This Matters

This project reflects practical, hands-on experience deploying enterprise-style perimeter security controls in a controlled lab environment.

It demonstrates the ability to:

* Translate security requirements into technical controls
* Validate effectiveness through logging and testing
* Implement proactive network defense mechanisms

---

## Future Improvements

* Integrate SIEM ingestion (Splunk / Sentinel)
* Automate alerting for high-severity blocks
* Create dashboard visualizations for executive reporting
* Implement VLAN-based policy segmentation

---

**Author:** Blessed
Cybersecurity Analyst | Blue Team Focused
Homelab Security Engineering Project

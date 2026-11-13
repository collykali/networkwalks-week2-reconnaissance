# Week 2: Footprinting and Reconnaissance Report

## 1. Report Metadata & Control Table
| Field | Detail |
| :--- | :--- |
| **Pentester Name (Cybersecurity Professional)** | Collins |
| **Program / Batch** | Networkwalks Cybersecurity Internship |
| **Date** | November 13, 2026 |
| **Modules Completed** | W2-PM1 (Footprinting Tools), W2-PM4 (theHarvester), W2-PM5 (Zenmap Scanning), W2-PM-FINAL (Report) |
| **Target System** | `networkwalks.com` (`192.232.216.135`) |

## 2. Executive Summary
This report documents the reconnaissance and footprinting activities conducted against `networkwalks.com` (IP: `192.232.216.135`) as part of the Networkwalks Cybersecurity Internship. The objective was to gather open-source intelligence (OSINT), map the external attack surface, identify running services and web technologies, and assess baseline exposure risks without causing disruption.

## 3. Reconnaissance & Target Summary
| Phase / Tool | Target / Parameter | Key Finding / Output Summary |
| :--- | :--- | :--- |
| **WHOIS Lookup** | `networkwalks.com` | Identified registrar details and authoritative name servers (`ns6135.hostgator.com`, `ns6136.hostgator.com`). |
| **Nslookup / DNS** | `192.232.216.135` | Resolved public domain to Unified Layer hosting infrastructure IP. |
| **WhatWeb** | CMS / Framework | Fingerprinted WordPress (`WordPress 7.0.4`) and WP Download Manager plugins. |
| **Wafw00f** | Firewall Detection | Confirmed active defense layer via **ModSecurity** (SpiderLabs). |
| **theHarvester** | OSINT / Subdomains | Harvested virtual hosts (`ftp`, `mail`, `webmail`, `webdisk`). |

### 3.1 Infrastructure & DNS Resolution
* **Tools used:** `whois`, `nslookup`
* **Commands:**
  ```bash
  whois networkwalks.com
  nslookup networkwalks.com

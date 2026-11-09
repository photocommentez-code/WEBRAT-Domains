# WEBRAT - Domains and C2 Infrastructure

This repository contains the domains and C2 IP addresses of WEBRAT.

It serves as an infrastructure log and threat intelligence feed for monitoring WEBRAT activity.

## Repository Structure

All threat indicators are located in the `domains/` directory:

* domains/domains.txt — Tracked domains used by WEBRAT for hosting, payload delivery, or communication.
* domains/IPs.txt — Command and Control (C2) server IP addresses.

## Usage and Integration

### Blocklists
Feed the raw lists directly into your DNS filters, firewalls, or proxy setups.

### SIEM / EDR Alerting
Import the IP addresses and domains into your security monitoring systems to hunt for active or historical connections.

```bash
# Example: Download the latest domains list
curl -O https://githubusercontent.com
```

## Disclaimer

IMPORTANT: The infrastructure listed in this repository is malicious. Interacting with these endpoints carries inherent risks. Use this data strictly for defensive, educational, and authorized security research purposes.

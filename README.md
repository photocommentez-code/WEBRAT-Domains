# WEBRAT

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
# Download the latest domains list
curl -O https://githubusercontent.com

# Download the latest C2 IPs list
curl -O https://githubusercontent.com
```

### Local Blocking (Hosts File)
You can block these malicious domains on your local computer by mapping them to a loopback address (127.0.0.1) in your system hosts file.

For Linux/macOS:
Append the domains to `/etc/hosts`

For Windows:
Append the domains to `C:\Windows\System32\drivers\etc\hosts`

## Disclaimer

IMPORTANT: The infrastructure listed in this repository is malicious. Interacting with these endpoints carries inherent risks. Use this data strictly for defensive, educational, and authorized security research purposes.

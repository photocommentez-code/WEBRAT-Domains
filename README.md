# Malware Infrastructure Indicators

This repository organizes defensive domain and IP indicators by malware family and category. It is intended for threat hunting, security monitoring, and carefully validated blocklists.

## Repository Structure

```text
Malware-As-a-Service/
|-- Loaders/
|   |-- Amadey/
|   |-- Bumblebee/
|   |-- PrivateLoader/
|   `-- SmokeLoader/
|-- Other/
|   |-- Remus/
|   |-- SilentNet/
|   |-- WeedHack/
|   |-- domains.txt
|   `-- IPs.txt
|-- Remote-Access-Trojans/
|   |-- AsyncRAT/
|   |-- DarkComet/
|   |-- NanoCore/
|   |-- NjRAT/
|   |-- QuasarRAT/
|   |-- Remcos/
|   `-- XWorm/
`-- Stealers/
	|-- AgentTesla/
	|-- BombayStealer/
	|-- Formbook/
	|-- Lumma/
	|-- RaccoonStealer/
	|-- RedLine/
	|-- Rhadamanthys/
	|-- SalatStealer/
	|-- StealC/
	`-- Vidar/
```

Each family directory has `domains.txt` and `IPs.txt`. The `Other` category also has catch-all lists. Categories are for repository organization; some families have overlapping capabilities or may be classified differently by other sources.

## Indicator Format

- Store one domain or IP address per line, without a URL scheme, path, or port.
- Lines beginning with `#` are comments and should be removed if the consuming tool does not support comments.
- Record the source and observation date in comments, and review indicators for accuracy and expiry before using them in production.
- The list files currently contain templates, not verified live C2 indicators.

## Defensive Use

Import validated indicators into DNS filtering, firewalls, proxies, or SIEM/EDR systems. Avoid directly visiting listed infrastructure. Confirm that an indicator is still relevant and not shared with legitimate services before blocking it.

## Disclaimer

Malware infrastructure can change ownership or be reassigned. Use indicators only for defensive, educational, and authorized security research, and validate them against trusted threat-intelligence sources before acting on them.

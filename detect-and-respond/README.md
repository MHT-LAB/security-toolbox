# Detect & Respond

Monitoring, alerting, and the tools SOC/blue-team work actually runs on.

## 🏆 Top 15 (most widely used)

- **[Wazuh](https://github.com/wazuh/wazuh)** — free, open-source SIEM and XDR platform.
  *Use it:* deploy the manager as a VM in your homelab, enroll a few agents on real endpoints, and tune out-of-the-box rules before layering custom ones — it's overkill to hand-roll detections before you've seen your own baseline noise.
- **[Security Onion](https://github.com/Security-Onion-Solutions/securityonion)** — Linux distro purpose-built for network security monitoring and threat hunting.
- **[Suricata](https://github.com/OISF/suricata)** — high-performance IDS/IPS and network security monitoring engine.
- **[Zeek](https://github.com/zeek/zeek)** — network traffic analysis framework; pairs well with a homelab SPAN/mirror port.
- **[OSSEC](https://github.com/ossec/ossec-hids)** — open-source host-based intrusion detection.
- **[Velociraptor](https://github.com/Velocidex/velociraptor)** — live endpoint DFIR and hunting, built on VQL queries.
- **[TheHive](https://github.com/TheHive-Project/TheHive)** — open-source security incident response / case-management platform.
- **[Cortex](https://github.com/TheHive-Project/Cortex)** — observable-analysis engine that pairs with TheHive for automated enrichment.
- **[Snort](https://github.com/snort3/snort3)** — the original open-source IDS/IPS, still widely deployed.
- **[Graylog](https://github.com/Graylog2/graylog2-server)** — centralized log management with a free tier that scales further than most homelabs need.
- **[OpenCTI](https://github.com/OpenCTI-Platform/opencti)** — open-source threat intel platform for structuring and correlating IOCs.
- **[MISP](https://github.com/MISP/MISP)** — open-source threat intelligence sharing platform.
- **[Arkime (Moloch)](https://github.com/arkime/arkime)** — full-packet-capture indexing and search at scale.
- **[Elastic Stack / Elastic Security](https://github.com/elastic/detection-rules)** — free-tier SIEM detections on top of the ELK stack.
- **[CrowdSec](https://github.com/crowdsecurity/crowdsec)** — collaborative, behavior-based intrusion detection with community threat-signal sharing.

## More tools worth knowing

- **[Fail2ban](https://github.com/fail2ban/fail2ban)** — bans IPs showing brute-force behavior in logs; the simplest homelab win in this whole list.
- **[Sigma](https://github.com/SigmaHQ/sigma)** — generic, vendor-agnostic detection-rule format; write once, convert to your SIEM's query language.
- **[Zircolite](https://github.com/wagga40/Zircolite)** — standalone Sigma rule matcher for EVTX/Windows event logs, no SIEM required.
- **[Sysmon config (SwiftOnSecurity)](https://github.com/SwiftOnSecurity/sysmon-config)** — battle-tested Sysmon configuration for meaningful Windows telemetry.
- **[HELK](https://github.com/Cyb3rWard0g/HELK)** — Elastic-based hunting platform with Spark/Jupyter for advanced analytics.
- **[RockNSM](https://github.com/rocknsm/rock)** — Zeek/Suricata-based network security monitoring distro.
- **[Malcolm](https://github.com/idaholab/Malcolm)** — Zeek/Suricata/Arkime bundle from Idaho National Lab, container-deployed.
- **[Stenographer](https://github.com/google/stenographer)** — Google's full-packet-capture buffer daemon for incident triage.
- **[Sagan](https://github.com/quadrantsec/sagan)** — high-performance log analysis engine, Snort-rule compatible.
- **[nfdump](https://github.com/phaag/nfdump)** — NetFlow collection and analysis toolset.
- **[p0f](https://github.com/p0f/p0f)** — passive OS/traffic fingerprinting from packet captures.
- **[GreyNoise (pygreynoise)](https://github.com/GreyNoise-Intelligence/pygreynoise)** — API client for filtering internet background noise out of alerts; free-tier SaaS.

*General infrastructure guidance:* stand up detection tooling on a SPAN/mirror port or agent-based collection so it's read-only against production traffic, route everything into one case-management tool (TheHive) rather than triaging in Slack/email, and treat every new rule as "tune against your own baseline for a week before it pages anyone."

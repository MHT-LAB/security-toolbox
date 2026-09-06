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

## Deception & honeypots

Tripwires that generate a high-confidence alert the moment someone touches them — no tuning, no baseline noise, because nothing legitimate should ever trigger one.

- **[Canarytokens](https://github.com/thinkst/canarytokens)** — Thinkst's free, self-hostable canary-token generator (also free-hosted at [canarytokens.org](https://canarytokens.org)); makes tripwire files, URLs, AWS keys, DNS records, etc. that alert on use.
  *Use it:* drop a handful into places an attacker would actually look — a fake `credentials.xlsx` on a file share, a bogus AWS key in a repo, a canary DNS record — and point the alert at email or Slack; this is the highest signal-to-effort detection you can add in an afternoon.
- **[OpenCanary](https://github.com/thinkst/opencanary)** — Thinkst's free, lightweight honeypot daemon that emulates common services (SSH, RDP, SMB, HTTP, etc.) and alerts on any interaction.
  *Use it:* run it on a spare VM/container on an internal VLAN with a hostname like a real server — any traffic to it at all is a real finding, feed alerts into the same pipeline as your SIEM (Wazuh/TheHive).
- **[Thinkst Canary](https://canary.tools)** — commercial hardware/virtual honeypot appliance from the same team behind Canarytokens/OpenCanary; no public repo, paid product.
- **[T-Pot](https://github.com/telekom-security/tpot)** — Deutsche Telekom's all-in-one honeypot platform, bundling 20+ honeypots (Cowrie, Dionaea, Conpot, etc.) behind one dashboard.
  *Use it:* stand it up on an isolated VM with a public-facing IP if you want real-world attack telemetry — never on the same network segment as anything that matters, it's designed to get hit.
- **[Cowrie](https://github.com/cowrie/cowrie)** — SSH/Telnet honeypot that logs full attacker sessions, including credentials tried and commands run.
- **[Dionaea](https://github.com/DinoTools/dionaea)** — malware-capturing honeypot that emulates vulnerable network services to collect dropped payloads.
- **[Conpot](https://github.com/mushorg/conpot)** — ICS/SCADA honeypot emulating industrial protocols (Modbus, S7comm); useful for OT-adjacent homelabs.
- **[HoneyTrap](https://github.com/honeytrap/honeytrap)** — modular, extensible honeypot framework for building custom low/medium-interaction traps.
- **[SNARE & TANNER](https://github.com/mushorg/snare)** — modern web-application honeypot pair (SNARE serves cloned pages, TANNER drives detection logic), successor to Glastopf.
- **[HoneyPy](https://github.com/foospidy/HoneyPy)** — low-interaction Python honeypot, easy to extend with new service plugins.
- **[Beeswarm](https://github.com/honeynet/beeswarm)** — pairs honeypots with "honeyclients" to catch credential theft in both directions.
- **[Wordpot](https://github.com/gbrindisi/wordpot)** — WordPress-specific honeypot for catching plugin/theme exploitation attempts.
- **[HFish](https://github.com/hacklcx/HFish)** — free honeypot deployment/management platform with a wide range of service probes and a central dashboard.

*Deception infrastructure guidance:* canary tokens cost nothing and belong everywhere (file shares, repos, inboxes, cloud credentials) — deploy those first. Full honeypots (T-Pot, Cowrie, Dionaea) need their own isolated VLAN or DMZ segment with no legitimate traffic and no route to production, since the entire point is that anything touching them is hostile; route every alert from both into the same case-management pipeline as the rest of this folder rather than a separate silo.

*General infrastructure guidance:* stand up detection tooling on a SPAN/mirror port or agent-based collection so it's read-only against production traffic, route everything into one case-management tool (TheHive) rather than triaging in Slack/email, and treat every new rule as "tune against your own baseline for a week before it pages anyone."

# Detect & Respond

Monitoring, alerting, and the tools SOC/blue-team work actually runs on.

Every tool below has its own page under [`tools/`](tools/) with Overview, Install/Deploy, Common Commands, a concrete Lab Exercise, and Related Tools — not just a link out.

## 🏆 Top 15 (most widely used)

| Tool | What it does |
|---|---|
| [Wazuh](tools/wazuh.md) | Free, open-source SIEM and XDR platform. |
| [Security Onion](tools/security-onion.md) | Linux distro purpose-built for network security monitoring. |
| [Suricata](tools/suricata.md) | High-performance IDS/IPS and network security monitoring engine. |
| [Zeek](tools/zeek.md) | Network traffic analysis framework. |
| [OSSEC](tools/ossec.md) | Open-source host-based intrusion detection. |
| [Velociraptor](tools/velociraptor.md) | Live endpoint DFIR and hunting, built on VQL queries. |
| [TheHive](tools/thehive.md) | Open-source security incident response / case-management platform. |
| [Cortex](tools/cortex.md) | Observable-analysis engine pairing with TheHive for enrichment. |
| [Snort](tools/snort.md) | The original open-source IDS/IPS, still widely deployed. |
| [Graylog](tools/graylog.md) | Centralized log management with a generous free tier. |
| [OpenCTI](tools/opencti.md) | Open-source threat intel platform for structuring and correlating IOCs. |
| [MISP](tools/misp.md) | Open-source threat intelligence sharing platform. |
| [Arkime (Moloch)](tools/arkime.md) | Full-packet-capture indexing and search at scale. |
| [Elastic Stack / Elastic Security](tools/elastic-stack.md) | Free-tier SIEM detections on top of the ELK stack. |
| [CrowdSec](tools/crowdsec.md) | Collaborative, behavior-based intrusion detection. |

## More tools worth knowing

| Tool | What it does |
|---|---|
| [Fail2ban](tools/fail2ban.md) | Bans IPs showing brute-force behavior in logs. |
| [Sigma](tools/sigma.md) | Generic, vendor-agnostic detection-rule format. |
| [Zircolite](tools/zircolite.md) | Standalone Sigma rule matcher for EVTX/Windows event logs. |
| [Sysmon config (SwiftOnSecurity)](tools/sysmon-config.md) | Battle-tested Sysmon configuration for meaningful telemetry. |
| [HELK](tools/helk.md) | Elastic-based hunting platform with Spark/Jupyter. |
| [RockNSM](tools/rocknsm.md) | Zeek/Suricata-based network security monitoring distro. |
| [Malcolm](tools/malcolm.md) | Zeek/Suricata/Arkime bundle from Idaho National Lab. |
| [Stenographer](tools/stenographer.md) | Google's full-packet-capture buffer daemon. |
| [Sagan](tools/sagan.md) | High-performance log analysis engine, Snort-rule compatible. |
| [nfdump](tools/nfdump.md) | NetFlow collection and analysis toolset. |
| [p0f](tools/p0f.md) | Passive OS/traffic fingerprinting from packet captures. |
| [GreyNoise (pygreynoise)](tools/greynoise.md) | Filters internet background noise out of alerts. |

## Deception & honeypots

Tripwires that generate a high-confidence alert the moment someone touches them — no tuning, no baseline noise, because nothing legitimate should ever trigger one.

| Tool | What it does |
|---|---|
| [Canarytokens](tools/canarytokens.md) | Free, self-hostable canary-token generator. |
| [OpenCanary](tools/opencanary.md) | Free, lightweight honeypot daemon emulating common services. |
| [Thinkst Canary](tools/thinkst-canary.md) | Commercial hardware/virtual honeypot appliance. |
| [T-Pot](tools/t-pot.md) | All-in-one honeypot platform bundling 20+ honeypots. |
| [Cowrie](tools/cowrie.md) | SSH/Telnet honeypot logging full attacker sessions. |
| [Dionaea](tools/dionaea.md) | Malware-capturing honeypot for network services. |
| [Conpot](tools/conpot.md) | ICS/SCADA honeypot emulating industrial protocols. |
| [HoneyTrap](tools/honeytrap.md) | Modular, extensible honeypot framework. |
| [SNARE & TANNER](tools/snare-tanner.md) | Modern web-application honeypot pair. |
| [HoneyPy](tools/honeypy.md) | Low-interaction Python honeypot, easy to extend. |
| [Beeswarm](tools/beeswarm.md) | Pairs honeypots with honeyclients for bidirectional detection. |
| [Wordpot](tools/wordpot.md) | WordPress-specific honeypot. |
| [HFish](tools/hfish.md) | Free honeypot deployment/management platform. |

*Deception infrastructure guidance:* canary tokens cost nothing and belong everywhere (file shares, repos, inboxes, cloud credentials) — deploy those first. Full honeypots ([T-Pot](tools/t-pot.md), [Cowrie](tools/cowrie.md), [Dionaea](tools/dionaea.md)) need their own isolated VLAN or DMZ segment with no legitimate traffic and no route to production, since the entire point is that anything touching them is hostile; route every alert from both into the same case-management pipeline as the rest of this folder ([TheHive](tools/thehive.md)) rather than a separate silo.

*General infrastructure guidance:* stand up detection tooling on a SPAN/mirror port or agent-based collection so it's read-only against production traffic, route everything into one case-management tool ([TheHive](tools/thehive.md)) rather than triaging in Slack/email, and treat every new rule as "tune against your own baseline for a week before it pages anyone."

# Threat Intel & Reference

ISACs, sharing communities, standards bodies, and vendor threat-intel feeds — where information moves between organizations rather than tools that run against a target.

Every tool below has its own page under [`tools/`](tools/) with Overview, Install/Deploy, Common Commands, a concrete Lab Exercise, and Related Tools — not just a link out. For this category "Install/Deploy" and "Common Commands" often mean "how to access or join" and "how to query the feed," since most entries are communities or reference sites rather than software.

## 🏆 Top 15 (most widely used)

| Tool | What it does |
|---|---|
| [National Council of ISACs](tools/national-council-of-isacs.md) | Directory of ISACs by sector; join the one for your industry. |
| [Cyber Threat Alliance](tools/cyber-threat-alliance.md) | Vendor-neutral nonprofit coordinating threat-intel sharing. |
| [CISA Automated Indicator Sharing (AIS)](tools/cisa-ais.md) | Free, real-time bidirectional indicator sharing with the US government. |
| [MISP](../detect-and-respond/tools/misp.md) | Open-source threat-intel platform *(page under detect-and-respond)*. |
| [Uncoder IO (SOC Prime)](tools/uncoder-io.md) | Free browser-based Sigma/Roota rule converter. |
| [LevelBlue Open Threat Exchange (OTX)](tools/otx.md) | Free, crowdsourced threat-intel sharing platform. |
| [CISA Cybersecurity Best Practices](tools/cisa-best-practices.md) | The US government's baseline security guidance hub. |
| [NIST Computer Security Resource Center (CSRC)](tools/nist-csrc.md) | Home of the NIST CSF, SP 800-series, and FIPS standards. |
| [InfraGard](tools/infragard.md) | FBI-affiliated public-private critical-infrastructure sharing partnership. |
| [SANS Internet Storm Center](tools/sans-isc.md) | Free daily threat diary and handler analysis. |
| [Cisco Talos Intelligence Group](tools/cisco-talos.md) | Free threat-intel research and reputation lookups. |
| [Spamhaus](tools/spamhaus.md) | Free DNSBL/blocklists for spam, malware, and botnet C2. |
| [MITRE ATT&CK](tools/mitre-attack.md) | The reference knowledge base of adversary tactics and techniques. |
| [abuse.ch](tools/abusech.md) | Free malware/botnet tracking feeds (MalwareBazaar, URLhaus, ThreatFox). |
| [CISA](tools/cisa.md) | Umbrella site for CISA advisories, alerts, and the KEV catalog. |

## More tools worth knowing

| Tool | What it does |
|---|---|
| [CrowdStrike Threat Intelligence](tools/crowdstrike-ti.md) | Commercial threat-intel and adversary-tracking service. |
| [Anomali ThreatStream](tools/anomali-threatstream.md) | Commercial threat-intelligence management platform. |
| [Mandiant (Google Cloud)](tools/mandiant.md) | Commercial threat-intel research and IR consulting. |
| [MS-ISAC Real-Time Indicator Feeds](tools/ms-isac-feeds.md) | Free automated indicator feed for SLTT government members. |

*General infrastructure guidance:* feed the free sources ([AIS](tools/cisa-ais.md), [OTX](tools/otx.md), [abuse.ch](tools/abusech.md), MISP feeds) into whatever platform you're already running in [`detect-and-respond/`](../detect-and-respond/README.md) ([MISP](../detect-and-respond/tools/misp.md), [OpenCTI](../detect-and-respond/tools/opencti.md)) so indicators become automated blocklist/detection updates instead of another tab to check manually; treat ISAC and InfraGard membership as a people-and-process investment, not a tool to deploy.

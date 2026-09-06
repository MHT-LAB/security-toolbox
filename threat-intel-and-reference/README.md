# Threat Intel & Reference

ISACs, sharing communities, standards bodies, and vendor threat-intel feeds — where information moves between organizations rather than tools that run against a target.

## 🏆 Top 15 (most widely used)

- **[National Council of ISACs](https://www.nationalisacs.org)** — directory of Information Sharing and Analysis Centers by sector; membership is usually free, join the one for your industry (e.g. financial services, healthcare).
  *Use it:* find your sector's ISAC and get an analyst or IT lead onto its mailing list/portal — most of the value here is the sector-specific advisory feed, not the directory page itself.
- **[Cyber Threat Alliance](https://www.cyberthreatalliance.org)** — vendor-neutral nonprofit coordinating threat-intel sharing across member security vendors.
- **[CISA Automated Indicator Sharing (AIS)](https://www.cisa.gov/ais)** — free, real-time bidirectional machine-to-machine indicator sharing with the US government.
  *Use it:* connect a TAXII client (e.g. through MISP or OpenCTI) to AIS to pull STIX-formatted indicators automatically rather than reading advisories by hand.
- **[MISP](https://www.misp-project.org)** — open-source threat-intel platform; also listed under [`detect-and-respond/`](../detect-and-respond/README.md) since it's both a feed consumer and a case tool.
- **[Uncoder IO (SOC Prime)](https://uncoder.io)** — free browser-based converter between Sigma, Roota, and native SIEM/EDR query languages.
- **[LevelBlue Open Threat Exchange (OTX)](https://otx.alienvault.com)** — free, crowdsourced threat-intel sharing platform (formerly AlienVault OTX).
- **[CISA Cybersecurity Best Practices](https://www.cisa.gov/topics/cybersecurity-best-practices)** — the US government's baseline guidance hub for organizational security practices.
- **[NIST Computer Security Resource Center (CSRC)](https://csrc.nist.gov)** — home of the NIST Cybersecurity Framework, SP 800-series, and FIPS standards.
  *Use it:* map your controls against NIST CSF or SP 800-53 once a year as a gap-check, even informally — it's the reference most auditors and cyber-insurance questionnaires already assume.
- **[InfraGard](https://www.infragard.org)** — FBI-affiliated public-private partnership for critical-infrastructure threat information sharing; free membership, vetting required.
- **[SANS Internet Storm Center](https://isc.sans.edu)** — free daily threat diary and handler analysis from the SANS community.
- **[Cisco Talos Intelligence Group](https://talosintelligence.com)** — free threat-intel research, IP/domain reputation lookups, and vulnerability disclosures.
- **[Spamhaus](https://www.spamhaus.org)** — free DNSBL/blocklists for spam, malware, and botnet C2 infrastructure.
- **[MITRE ATT&CK](https://attack.mitre.org)** — the reference knowledge base of adversary tactics and techniques (the [Navigator](https://github.com/mitre-attack/attack-navigator) app is in [`learn-and-practice/`](../learn-and-practice/README.md)).
- **[abuse.ch](https://abuse.ch)** — free malware/botnet tracking feeds (MalwareBazaar, URLhaus, Feodo Tracker, ThreatFox).
- **[CISA](https://www.cisa.gov)** — the umbrella site for the above CISA resources: advisories, alerts, and known-exploited-vulnerabilities catalog.

## More tools worth knowing

- **[CrowdStrike Threat Intelligence](https://www.crowdstrike.com/platform/threat-intelligence/)** — commercial threat-intel and adversary-tracking service.
- **[Anomali ThreatStream](https://www.anomali.com/products/threatstream)** — commercial threat-intelligence management platform.
- **[Mandiant (Google Cloud)](https://cloud.google.com/security/mandiant)** — commercial threat-intel research and incident-response consulting.

*General infrastructure guidance:* feed the free sources (AIS, OTX, abuse.ch, MISP feeds) into whatever platform you're already running in [`detect-and-respond/`](../detect-and-respond/README.md) (MISP, OpenCTI) so indicators become automated blocklist/detection updates instead of another tab to check manually; treat ISAC and InfraGard membership as a people-and-process investment, not a tool to deploy.

# Learn & Practice

Hands-on ranges, CTFs, and reference material for building the muscle.

Every tool below has its own page under [`tools/`](tools/) with Overview, Install/Deploy, Common Commands, a concrete Lab Exercise, and Related Tools — not just a link out.

## 🏆 Top 15 (most widely used)

| Tool | What it does |
|---|---|
| [TryHackMe](tools/tryhackme.md) | Guided, hands-on rooms; free tier covers most fundamentals. |
| [Hack The Box](tools/hack-the-box.md) | Pentesting labs and machines; free tier available. |
| [OverTheWire Wargames](tools/overthewire.md) | Free wargames for Linux, SSH, and security fundamentals. |
| [picoCTF](tools/picoctf.md) | Free, beginner-friendly CTF platform built by Carnegie Mellon. |
| [VulnHub](tools/vulnhub.md) | Free downloadable vulnerable VMs for practice. |
| [LetsDefend](tools/letsdefend.md) | Free-tier SOC analyst simulation platform. |
| [CyberDefenders](tools/cyberdefenders.md) | Free blue-team DFIR challenges. |
| [MITRE ATT&CK Navigator](tools/mitre-attack-navigator.md) | Browser-based technique mapping against ATT&CK. |
| [Metasploitable3](../test-and-exploit/tools/metasploitable3.md) | Intentionally vulnerable VM, the standard first target *(page under test-and-exploit)*. |
| [DVWA](../test-and-exploit/tools/dvwa.md) | Adjustable-difficulty web target *(page under test-and-exploit)*. |
| [WebGoat](../test-and-exploit/tools/webgoat.md) | OWASP's guided, lesson-based insecure training app *(page under test-and-exploit)*. |
| [Juice Shop](../test-and-exploit/tools/juice-shop.md) | OWASP's modern intentionally-vulnerable app *(page under test-and-exploit)*. |
| [OWASP Security Shepherd](tools/owasp-security-shepherd.md) | Web/mobile app security training platform. |
| [CTFd](tools/ctfd.md) | The standard open-source platform for hosting your own CTF. |
| [PentesterLab](tools/pentesterlab.md) | Hands-on web/exploit-focused exercises. |

## More tools worth knowing

| Tool | What it does |
|---|---|
| [rCTF](tools/rctf.md) | Lightweight, scalable open-source CTF platform. |
| [DetectionLab](tools/detectionlab.md) | Vagrant/Packer-built AD lab pre-wired with logging/detection tooling. |
| [GOAD (Game of Active Directory)](tools/goad.md) | Vulnerable-by-design AD lab for practicing attack paths. |
| [Vulnerable-AD](tools/vulnerable-ad.md) | Scripts to build a deliberately misconfigured AD environment. |
| [Damn Vulnerable Web Services (DVWS)](tools/dvws.md) | Vulnerable SOAP/REST API target. |
| [bWAPP](tools/bwapp.md) | "Buggy web application" covering 100+ vulnerability classes. |
| [DVIA-v2](tools/dvia-v2.md) | Damn Vulnerable iOS App, for mobile security practice. |
| [OVAA](tools/ovaa.md) | Oversecured Vulnerable Android App, for mobile security practice. |
| [Root-Me](tools/root-me.md) | Long-running free challenge site across many security domains. |
| [CTFtime](tools/ctftime.md) | Event tracker/ratings for competitive CTF teams. |

*General infrastructure guidance:* build the AD/web/network labs above ([DetectionLab](tools/detectionlab.md), [GOAD](tools/goad.md), [Metasploitable3](../test-and-exploit/tools/metasploitable3.md)) on the same isolated hypervisor network used for [`test-and-exploit/`](../test-and-exploit/README.md), and log everything to a [`detect-and-respond/`](../detect-and-respond/README.md) stack (Wazuh/Security Onion) so practice attacks double as practice detections.

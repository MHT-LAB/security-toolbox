# Learn & Practice

Hands-on ranges, CTFs, and reference material for building the muscle.

## 🏆 Top 15 (most widely used)

- **[TryHackMe](https://tryhackme.com)** — guided, hands-on rooms; free tier covers most fundamentals. SaaS, no public repo.
  *Use it:* work rooms in order within a learning path (e.g. "Pre Security" → "Jr Penetration Tester"), not at random — the guided structure is the actual value over raw HTB-style boxes.
- **[Hack The Box](https://www.hackthebox.com)** — pentesting labs and machines; free tier available. SaaS, no public repo.
- **[OverTheWire Wargames](https://overthewire.org/wargames/)** — free wargames for Linux, SSH, and security fundamentals. Site-hosted, no central repo.
- **[picoCTF](https://github.com/picoCTF/picoCTF)** — free, beginner-friendly CTF platform built by Carnegie Mellon; platform itself is open source.
- **[VulnHub](https://www.vulnhub.com)** — free downloadable vulnerable VMs for practice. Archive site, no active repo.
- **[LetsDefend](https://letsdefend.io)** — free-tier SOC analyst simulation platform. SaaS.
- **[CyberDefenders](https://cyberdefenders.org)** — free blue-team DFIR challenges. SaaS.
- **[MITRE ATT&CK Navigator](https://github.com/mitre-attack/attack-navigator)** — browser-based technique mapping against the ATT&CK framework.
- **[Metasploitable3](https://github.com/rapid7/metasploitable3)** — intentionally vulnerable VM, the standard first target for offensive-tool practice.
- **[DVWA](https://github.com/digininja/DVWA)** — Damn Vulnerable Web Application, a local standard for web attack fundamentals.
- **[WebGoat](https://github.com/WebGoat/WebGoat)** — OWASP's deliberately insecure training web app.
- **[Juice Shop](https://github.com/juice-shop/juice-shop)** — OWASP's modern intentionally-vulnerable web app; good next step after DVWA/WebGoat.
- **[OWASP Security Shepherd](https://github.com/OWASP/SecurityShepherd)** — web/mobile app security training platform with progressive challenges.
- **[CTFd](https://github.com/CTFd/CTFd)** — the standard open-source platform for hosting your own CTF.
- **[PentesterLab](https://pentesterlab.com)** — hands-on web/exploit-focused exercises; has free content, mostly paid. SaaS.

## More tools worth knowing

- **[rCTF](https://github.com/redpwn/rctf)** — lightweight, scalable open-source CTF platform (used by redpwn/Ubiquity).
- **[DetectionLab](https://github.com/clong/DetectionLab)** — Vagrant/Packer-built AD lab pre-wired with logging/detection tooling — ideal for practicing blue-team work end to end.
- **[GOAD (Game of Active Directory)](https://github.com/Orange-Cyberdefense/GOAD)** — vulnerable-by-design Active Directory lab for practicing AD attack paths.
- **[Vulnerable-AD](https://github.com/WazeHell/vulnerable-AD)** — scripts to build a deliberately misconfigured AD environment for practice.
- **[Damn Vulnerable Web Services (DVWS)](https://github.com/snoopysecurity/dvws)** — vulnerable SOAP/REST API target for web-service security testing.
- **[bWAPP](https://github.com/ismailtasdelen/bWAPP)** — "buggy web application" covering 100+ vulnerability classes.
- **[DVIA-v2](https://github.com/prateek147/DVIA-v2)** — Damn Vulnerable iOS App, for mobile security practice.
- **[OVAA](https://github.com/oversecured/ovaa)** — Oversecured Vulnerable Android App, for mobile security practice.
- **[Root-Me](https://www.root-me.org)** — long-running free challenge site across many security domains. Site-hosted.
- **[CTFtime](https://ctftime.org)** — event tracker/ratings for competitive CTF teams; the reference calendar for the CTF scene.

*General infrastructure guidance:* build the AD/web/network labs above (DetectionLab, GOAD, Metasploitable3) on the same isolated hypervisor network used for [`test-and-exploit/`](../test-and-exploit/README.md), and log everything to a [`detect-and-respond/`](../detect-and-respond/README.md) stack (Wazuh/Security Onion) so practice attacks double as practice detections.

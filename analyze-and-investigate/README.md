# Analyze & Investigate

Forensics, malware analysis, and pulling the real story out of an artifact.

Every tool below has its own page under [`tools/`](tools/) with Overview, Install/Deploy, Common Commands, a concrete Lab Exercise, and Related Tools — not just a link out.

## 🏆 Top 15 (most widely used)

| Tool | What it does |
|---|---|
| [Wireshark](tools/wireshark.md) | The standard for packet capture and protocol analysis. |
| [Autopsy](tools/autopsy.md) | Free digital forensics platform (GUI for The Sleuth Kit). |
| [The Sleuth Kit](tools/sleuthkit.md) | Command-line disk/file-system forensics library. |
| [Volatility 3](tools/volatility3.md) | Memory forensics framework. |
| [YARA](tools/yara.md) | Pattern-matching for identifying and classifying malware. |
| [CAPEv2](tools/capev2.md) | Automated malware analysis sandbox (Cuckoo successor). |
| [Cuckoo Sandbox](tools/cuckoo-sandbox.md) | The original open-source automated malware sandbox. |
| [Ghidra](tools/ghidra.md) | NSA's free software reverse-engineering suite. |
| [radare2](tools/radare2.md) | Command-line reverse-engineering framework. |
| [Cutter](tools/cutter.md) | GUI front end for radare2/Rizin. |
| [x64dbg](tools/x64dbg.md) | Open-source user-mode Windows debugger. |
| [REMnux](tools/remnux.md) | Linux distro pre-loaded for malware analysis. |
| [Plaso / log2timeline](tools/plaso.md) | Builds super-timelines from forensic artifacts. |
| [CyberChef](tools/cyberchef.md) | GCHQ's "cyber Swiss Army knife" for decoding/transforming data. |
| [MISP](../detect-and-respond/tools/misp.md) | Threat-intel platform, doubles as IOC correlation during investigations *(page under detect-and-respond)*. |

## More tools worth knowing

| Tool | What it does |
|---|---|
| [Timesketch](tools/timesketch.md) | Collaborative timeline analysis, pairs with Plaso. |
| [Bulk Extractor](tools/bulk-extractor.md) | Scans disk images/files for artifacts without file-system parsing. |
| [RegRipper](tools/regripper.md) | Windows registry parsing and analysis. |
| [Eric Zimmerman's Tools (EZ Tools)](tools/ez-tools.md) | The standard suite for Windows DFIR artifact parsing. |
| [Chainsaw](tools/chainsaw.md) | Rapid triage/hunting over Windows event logs using Sigma. |
| [Hayabusa](tools/hayabusa.md) | Fast Windows event log timeline/detection tool. |
| [Loki](tools/loki.md) | Simple IOC and YARA scanner for compromise indicators. |
| [Fenrir](tools/fenrir.md) | Bash-based IOC scanner for *nix hosts, no dependencies. |
| [binwalk](tools/binwalk.md) | Firmware analysis and extraction tool. |
| [Detect It Easy (DIE)](tools/detect-it-easy.md) | File-type and packer detection for binaries. |
| [FLARE-VM](tools/flare-vm.md) | Mandiant's Windows VM configuration for reverse engineering. |
| [FLOSS](tools/floss.md) | Extracts obfuscated strings from malware binaries. |
| [Arsenal Image Mounter](tools/arsenal-image-mounter.md) | Mounts forensic disk images as drives on Windows. |
| [VirusTotal](tools/virustotal.md) | Free multi-engine file/URL/hash reputation lookup. |
| [JoeSandbox](tools/joesandbox.md) | Commercial automated malware sandbox, free community tier. |
| [Hybrid Analysis](tools/hybrid-analysis.md) | Free, CrowdStrike-run automated malware sandbox. |
| [MxToolbox Email Header Analyzer](tools/mxtoolbox-email-header.md) | Free RFC822 email-header parser. |

*General infrastructure guidance:* run malware sandboxes ([CAPEv2](tools/capev2.md)/[Cuckoo](tools/cuckoo-sandbox.md), [REMnux](tools/remnux.md)) on isolated hosts with no route back to production — a dedicated hypervisor VLAN with host-only networking is standard. Work from disk-image copies and hash-verify them before and after analysis; never analyze on the source drive.

# Analyze & Investigate

Forensics, malware analysis, and pulling the real story out of an artifact.

## 🏆 Top 15 (most widely used)

- **[Wireshark](https://github.com/wireshark/wireshark)** — the standard for packet capture and protocol analysis.
  *Use it:* capture on a mirrored port or a saved .pcap, never live on a production interface you don't control — filter with display filters before you scroll, not after.
- **[Autopsy](https://github.com/sleuthkit/autopsy)** — free digital forensics platform (GUI for The Sleuth Kit).
- **[The Sleuth Kit](https://github.com/sleuthkit/sleuthkit)** — command-line disk/file-system forensics library underlying Autopsy.
- **[Volatility 3](https://github.com/volatilityfoundation/volatility3)** — memory forensics framework.
- **[YARA](https://github.com/VirusTotal/yara)** — pattern-matching for identifying and classifying malware.
- **[CAPEv2](https://github.com/kevoreilly/CAPEv2)** — automated malware analysis sandbox (Cuckoo successor).
- **[Cuckoo Sandbox](https://github.com/cuckoosandbox/cuckoo)** — the original open-source automated malware sandbox CAPE forked from.
- **[Ghidra](https://github.com/NationalSecurityAgency/ghidra)** — NSA's free software reverse-engineering suite.
- **[radare2](https://github.com/radareorg/radare2)** — command-line reverse-engineering framework.
- **[Cutter](https://github.com/rizinorg/cutter)** — GUI front end for radare2/Rizin, much friendlier for daily RE work.
- **[x64dbg](https://github.com/x64dbg/x64dbg)** — open-source user-mode Windows debugger.
- **[REMnux](https://github.com/REMnux/remnux)** — Linux distro pre-loaded for malware analysis.
- **[Plaso / log2timeline](https://github.com/log2timeline/plaso)** — builds super-timelines from forensic artifacts across a whole system.
- **[CyberChef](https://github.com/gchq/CyberChef)** — GCHQ's "cyber Swiss Army knife" for decoding/transforming data, runs entirely in-browser.
- **[MISP](https://github.com/MISP/MISP)** — threat-intel platform, doubles as an IOC correlation tool during investigations.

## More tools worth knowing

- **[Timesketch](https://github.com/google/timesketch)** — collaborative timeline analysis, pairs with Plaso output.
- **[Bulk Extractor](https://github.com/simsong/bulk_extractor)** — scans disk images/files for emails, URLs, and other artifacts without parsing the file system.
- **[RegRipper](https://github.com/keydet89/RegRipper3.0)** — Windows registry parsing and analysis.
- **[Eric Zimmerman's Tools (EZ Tools)](https://github.com/EricZimmerman)** — the de facto standard suite for Windows DFIR artifact parsing (MFTECmd, Registry Explorer, Timeline Explorer, etc.).
- **[Chainsaw](https://github.com/WithSecureLabs/chainsaw)** — rapid triage/hunting over Windows event logs using Sigma rules.
- **[Hayabusa](https://github.com/Yamato-Security/hayabusa)** — fast Windows event log timeline/detection tool, Sigma-compatible.
- **[Loki](https://github.com/Neo23x0/Loki)** — simple IOC and YARA scanner for compromise indicators.
- **[Fenrir](https://github.com/Neo23x0/Fenrir)** — bash-based IOC scanner for *nix hosts, no dependencies to install.
- **[binwalk](https://github.com/ReFirmLabs/binwalk)** — firmware analysis and extraction tool.
- **[Detect It Easy (DIE)](https://github.com/horsicq/Detect-It-Easy)** — file-type and packer detection for binaries.
- **[FLARE-VM](https://github.com/mandiant/flare-vm)** — Mandiant's Windows VM configuration for reverse engineering and malware analysis.
- **[FLOSS](https://github.com/mandiant/flare-floss)** — extracts obfuscated strings from malware binaries.
- **[Arsenal Image Mounter](https://github.com/ArsenalRecon/Arsenal-Image-Mounter)** — mounts forensic disk images as drives on Windows for native tool access.

*General infrastructure guidance:* run malware sandboxes (CAPE/Cuckoo, REMnux) on isolated hosts with no route back to production — a dedicated hypervisor VLAN with host-only networking is standard. Work from disk-image copies and hash-verify them before and after analysis; never analyze on the source drive.

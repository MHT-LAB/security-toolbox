# Wireshark

The standard for packet capture and protocol analysis — dissects hundreds of protocols and lets you filter/follow individual streams from a live capture or saved pcap.

**Links:** [GitHub](https://github.com/wireshark/wireshark) · [Docs](https://www.wireshark.org/docs/)

## Overview

Wireshark is the GUI reference for looking at what actually happened on the wire — display filters narrow a huge capture down to the relevant packets, "Follow Stream" reconstructs a full TCP conversation, and protocol dissectors decode everything from HTTP to Kerberos.

## Install / Deploy

```bash
sudo apt install wireshark
# Add your user to the wireshark group to capture without root:
sudo usermod -aG wireshark $USER
```

## Common Commands

Wireshark is GUI-driven; common display filters:
```text
http.request
ip.addr == 10.0.0.5
tcp.port == 445 && smb2
```

## Lab Exercise

Capture on a mirrored port or a saved .pcap, never live on a production interface you don't control. Run [Responder](../../test-and-exploit/tools/responder.md) in your lab while capturing with Wireshark, then filter for `ntlmssp` to see the captured NTLM exchange directly on the wire.

## Related Tools

- [Zeek](../../detect-and-respond/tools/zeek.md) — structured-log alternative for the same traffic
- [Arkime](../../detect-and-respond/tools/arkime.md) — full-capture indexing at scale

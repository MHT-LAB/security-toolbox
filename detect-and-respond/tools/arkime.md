# Arkime (Moloch)

Full-packet-capture indexing and search at scale — stores and indexes complete network traffic so you can query and replay sessions, not just alerts.

**Links:** [GitHub](https://github.com/arkime/arkime) · [Docs](https://arkime.com/docs)

## Overview

Where Suricata/Zeek generate metadata and alerts, Arkime stores the actual packets and indexes them for fast search — "show me every session between these two IPs last Tuesday" and then let you download and replay the pcap. It's the tool you reach for after an alert, to see exactly what happened on the wire.

## Install / Deploy

```bash
# Official install script (Debian/Ubuntu/CentOS supported):
wget https://github.com/arkime/arkime/releases/latest/download/arkime_<version>_amd64.deb
sudo dpkg -i arkime_<version>_amd64.deb
sudo /opt/arkime/bin/Configure
```

## Common Commands

```bash
/opt/arkime/db/db.pl <es-host>:9200 init
/opt/arkime/bin/capture -c /opt/arkime/etc/config.ini
```

## Lab Exercise

Deploy Arkime on the same SPAN port as Suricata/Zeek in your lab, generate an alert-worthy event, then use Arkime's search UI to find and download the exact session as a pcap for deeper review in [Wireshark](../../analyze-and-investigate/tools/wireshark.md).

## Related Tools

- [Wireshark](../../analyze-and-investigate/tools/wireshark.md) — deep-dive on a session Arkime surfaces
- [Zeek](zeek.md) · [Suricata](suricata.md) — typically deployed alongside it

# Velociraptor

Live endpoint DFIR and hunting, built on VQL (Velociraptor Query Language) — query hundreds of endpoints simultaneously for artifacts, without waiting for a full forensic image.

**Links:** [GitHub](https://github.com/Velocidex/velociraptor) · [Docs](https://docs.velociraptor.app)

## Overview

Velociraptor deploys a lightweight agent that responds to VQL queries from a central server — "show me every process with a network connection on all 200 endpoints right now" runs in seconds. It's the tool for scaling DFIR beyond one-machine-at-a-time triage.

## Install / Deploy

```bash
# Download the release binary, then:
./velociraptor config generate -i     # interactive server config
./velociraptor --config server.config.yaml frontend
```

## Common Commands

```text
# In the web UI, run a VQL query, e.g.:
SELECT * FROM pslist() WHERE Name =~ "mimikatz"
SELECT * FROM glob(globs="C:/Users/*/AppData/**/*.exe")
```

## Lab Exercise

Deploy the server and enroll a couple of lab Windows/Linux VMs as clients, then run a VQL hunt (`pslist()`) across both simultaneously after running something suspicious (e.g. [Mimikatz](../../test-and-exploit/tools/mimikatz.md)) on one, to see the live-query model in action.

## Related Tools

- [TheHive](thehive.md) — route findings here for case management
- [Chainsaw](../../analyze-and-investigate/tools/chainsaw.md) — complementary offline log triage

# EyeWitness

Screenshots websites and reports server info/default creds — similar goal to Aquatone, with a stronger focus on flagging default credential pages.

**Links:** [GitHub](https://github.com/FortyNorthSecurity/EyeWitness)

## Overview

EyeWitness screenshots a list of URLs and, notably, tries to categorize pages by type (login page, default install page) and cross-references against a database of common default credentials for identified software.

## Install / Deploy

```bash
git clone https://github.com/FortyNorthSecurity/EyeWitness.git
cd EyeWitness/Python/setup && ./setup.sh
```

## Common Commands

```bash
python3 EyeWitness.py -f urls.txt --web
python3 EyeWitness.py --single https://target --web
```

## Lab Exercise

Run EyeWitness against a list of hosts discovered in your lab (e.g. a homelab network scan) and review its categorized report for anything flagged as a default-credential login page.

## Related Tools

- [Aquatone](aquatone.md) — similar screenshot-gallery alternative

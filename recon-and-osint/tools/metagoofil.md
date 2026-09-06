# Metagoofil

Extracts metadata from public documents (PDF, DOCX, XLSX, PPTX) — author names, software versions, and paths that leak internal information.

**Links:** [GitHub](https://github.com/opsdisk/metagoofil)

## Overview

Metagoofil searches for public documents on a target domain (via search-engine dorking) and pulls embedded metadata — usernames, internal file paths, and software versions — that can reveal naming conventions or internal structure useful for later social-engineering or password-spray work.

## Install / Deploy

```bash
git clone https://github.com/opsdisk/metagoofil.git
cd metagoofil && pip install -r requirements.txt
```

## Common Commands

```bash
python3 metagoofil.py -d example.com -t pdf,docx -l 50 -n 10 -o results -f results.html
```

## Lab Exercise

Run Metagoofil against a domain with publicly posted PDFs/DOCX files you control, and check whether the extracted metadata reveals more than you expected (usernames, internal software versions) — then strip that metadata before publishing similar files for real.

## Related Tools

- [theHarvester](theharvester.md) — complementary email/subdomain OSINT

# blocklists

DNS blocklists generated from public ad/tracker filter sources. Built as an
approximation of Filtr-style (Wipr) coverage for use at the DNS level, where
per-URL filtering isn't available.

## Lists

- **ublock-nextdns-blocklist.txt** — 94,864 domains, plain one-per-line format
  for NextDNS (Denylist → Add a blocklist). Generated 2026-10-07 from:
  - uBlock Origin filters
  - uBlock Origin – Badware risks
  - uBlock Origin – Privacy
  - uBlock Origin 2026 filters
  - EasyList
  - EasyPrivacy
  - Peter Lowe's Ad and tracking server list

## Use with NextDNS

1. Open my.nextdns.io → your profile → **Denylist**.
2. Click **Add a blocklist** and paste the raw URL of the list file:
   `https://raw.githubusercontent.com/garyengel/blocklists/main/ublock-nextdns-blocklist.txt`
3. Save. NextDNS refreshes it automatically.

## Limitations

- DNS blocking works on whole domains; it can't do the per-URL precision of
  Filtr or a browser content blocker.
- Ads served from a service's own domain (YouTube, Instagram, etc.) can't be
  blocked at DNS level without breaking the service.
- Regenerate periodically; filter sources update constantly. The generator
  script lives in the ai-studio repo (`scripts/ublock-ios-blocklist.sh`).

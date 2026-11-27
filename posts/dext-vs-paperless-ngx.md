# Receipt & invoice capture: Dext vs Paperless-ngx (paid vs free)

**27 Nov 2026** · Prices as of 27 Nov 2026 (dext.com, US page, USD, excl. tax). Check the official pages before you buy; prices change.

| | Dext Business (paid) | Paperless-ngx (free, open source) |
|---|---|---|
| What it is | Cloud receipt, bill and invoice capture that extracts the data and pushes it to your accounting software | Self-hosted document archive: scan, OCR, tag, search |
| Price | US$25.21/month on annual billing (US$302.50/year); 14-day free trial, no card | $0 (GPL-3.0 licence). You pay for your own server/storage |
| Allowance | 250 documents/month, 5 users | No document limit set by the software |
| Included free credits | 10 sheets bank statement extraction, 5 line-item documents, 5 supplier statements | — |
| Add-ons | AI Assist US$10.50/mo (price shown until 31 Jan 2027) · Bank statement extraction from US$13/mo or US$0.32/doc · Line items from US$20.50/mo or US$0.50/doc · Supplier statements from US$20.50/mo or US$0.50/doc | None — you run, update and back up the server |
| OCR / extraction | Automatic data extraction for accounting | Tesseract OCR, 100+ languages; stores PDF/A + the original |
| Organising | Pushes coded data to your ledger | Machine-learning auto-tags (tags, correspondent, document type), full-text search, email import, workflows |
| Where files live | Dext cloud | Your own server |
| Setup | Sign up and connect your accounting software | Docker; one-line install script (below) |

## Paperless-ngx install (from the official README)

```
bash -c "$(curl -L https://raw.githubusercontent.com/paperless-ngx/paperless-ngx/main/install-paperless-ngx.sh)"
```

Security note from the README: "Paperless-ngx should never be run on an untrusted host because information is stored in clear text without encryption." Run it on a server you control and keep backups.

## Who should pick which

- **Dext** — you want receipts and bills turned into extracted, coded data in your ledger, with no IT work.
- **Paperless-ngx** — you need a searchable in-house archive of bills, receipts and supplier statements at $0, and someone on the team can run Docker.
- Paperless-ngx is **not** a bookkeeping tool: it does not post to your ledger.
- Test either one with demo receipts first, never live client files.

## Links

- Dext Business pricing: https://dext.com/us/business/pricing
- Paperless-ngx on GitHub (by the Paperless-ngx community; 48.6k stars, GPL-3.0, updated 27 Nov 2026): https://github.com/paperless-ngx/paperless-ngx
- Paperless-ngx docs: https://docs.paperless-ngx.com/
- PDF guide: [Receipt Capture: Paid vs Free Guide](../freebies/Receipt-Capture-Paid-vs-Free-Guide.pdf)

## Sources

dext.com/us/business/pricing (checked 27 Nov 2026) · github.com/paperless-ngx/paperless-ngx README and GitHub API (27 Nov 2026) · docs.paperless-ngx.com (27 Nov 2026)

---

By Abu Daud, CMA · WhatsApp +966 57 561 5384

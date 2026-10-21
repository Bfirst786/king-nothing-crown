# King Nothing Cyber Crown

A modular 3D-printed cyber crown for a Halloween costume, built as a test bed for the Home Fab System (HFS). Prototype before wearable use: nothing here is a certified wearable electronics design, and the builder owns final electrical, battery, thermal and mechanical validation.

Start with `docs/Project_Brief_and_Design_Definition_v0.1.md`. It is the authority on intent, locked decisions, requirements and open interfaces. If another file disagrees with it, the brief wins until a change request says otherwise.

## Where each master lives

| Kind of file | Master | Notes |
|--------------|--------|-------|
| Brief, logs, notes, code, schematics, BOM, test records | This repo | Text and code only |
| CAD source, STL/3MF, scans, photos, reference images, PDFs | Google Drive, `KING NOTHING` folder | Binaries stay out of git; link to them from the repo |
| Working copy for Claude sessions | The KING NOTHING Claude project | Refreshed from this repo, never edited |
| Validated, reusable outputs | The `hfs` repo, after extraction | Filed under Knowledge, Shop or Business; nothing is published straight from this repo |

If a copy elsewhere disagrees with this repo, this repo wins.

## Layout

- `docs/` brief, change-request log, decision log
- `cad/` parameter lists and Fusion export notes (binaries in Drive)
- `firmware/` ESP32-S3 code and asset-conversion scripts
- `electronics/` schematics, pin maps, BOM
- `fabrication/` print profiles and the assembly traveler
- `testlog/` measurements, results and photo links
- `hfs/` HFS notes, divergence records and extraction candidates

## Rules

- Shared interfaces and locked items change only through a change request (see the brief, section 9).
- Every significant decision gets an HFS note: followed, diverged, or new (see `hfs/README.md`).
- Tag claims by evidence level and decisions by maturity, as the brief does.
- Do not commit lyrics, credentials or customer data.

# King Nothing Cyber Crown: Project Brief & Design Definition v0.1

Status: DRAFT for Brian's review | Date: 2026-10-20 | Owner: Brian | Maintained in: Chat 00, Design Director & Source of Truth

This is the authoritative statement of intent, locked decisions, requirements and open interfaces. If another document disagrees with it, this brief wins until a change request says otherwise. Built from the Build Manual v0.1, Universal Module Study v0.1, Project Setup Guide v0.1, the HFS design-process analysis and seed, and Brian's statements in chat. It was not rebuilt from the image studies; the cover image remains the visual authority.

## How to read the tags

Decision maturity: **Open** (insufficient evidence), **Preferred** (current direction, cheap to reverse), **Prov. locked** (build against it, a named test remains), **Locked** (change needs a change request), **Obsolete**.

Evidence level: **INS** inspiration, **VIS** visual concept, **ASM** reasoned assumption, **SPEC** supplier specification, **BENCH** bench measurement, **PROTO** prototype observation, **INTEG** integrated test, **FIELD** use validation. Generated images and plausible engineering suggestions stay at VIS or ASM until verified against a part or document.

## 1. Intent and experience

A Halloween costume inspired by the themes around Metallica's "King of Nothing": status and fashion set against emptiness and impermanence. The wearer is a structured, designer-looking figure under a veil, crowned with an architectural cyber crown. The crown should read as intentional and complete with every screen dark. Literal lyrics are not used as design vocabulary and are not embedded in any asset.

Wearer: Brian. Fabrication: 3D printing (PETG or ASA shell, TPU comfort pads). Deadline: Halloween. If the event is 31 October, 11 days remain from today, which makes the fallback ladder (section 3) the real plan, not a footnote.

## 2. Design grammar

| ID | Element | Maturity | Evidence |
|----|---------|----------|----------|
| DG-01 | The "King Nothing" cover image is the locked crown design (crown on a veiled wearer) | Locked | VIS |
| DG-02 | Tall forked front element is the centerpiece; the wide split stays open for about two thirds of the fork height before joining | Locked | VIS |
| DG-03 | Two-tone weathered metal finish; architectural surfaces, recesses, fasteners, material transitions, selective abrasion | Locked | VIS |
| DG-04 | No filigree | Locked | VIS |
| DG-05 | Two hero media modules flank the fork: one TV-like bezel, one phone-like bezel, same TFT hardware inside | Locked | VIS/ASM |
| DG-06 | Remaining spoke bases take nominal 2 x 2 inch motif modules (passive relief, lit glyph, or TFT) | Prov. locked | ASM |
| DG-07 | Clean base band holds wire runs, electronics and docking ports, concealed by decorative plugs | Preferred | ASM |
| DG-08 | Spires are individual elements assembled after printing | Preferred | ASM |
| DG-09 | Module look from the cover image; general layout and rear modules from the v0.3 reference sheet | Preferred | VIS |
| DG-10 | Four main spikes (including the hero front) plus minor spikes; slight asymmetry acceptable | Preferred | VIS |
| DG-11 | Crown looks finished unlit; a non-lit minimalist completion path stays available | Locked | VIS |
| DG-12 | Garment language: black turtleneck, mandarin-collar jacket, loose sheer veil (alternatives to the hood still open) | Open | VIS |

## 3. Configurations and fallback ladder

One mechanical platform, designed for B and electrically populated for A.

- **Design A (primary):** 2 hero TFTs, 4 to 6 passive or backlit motif panels, one ESP32-S3, addressable lighting.
- **Design B (expansion):** A plus 4 to 6 motif TFTs on a second ESP32-S3, lighting by zone. Not required for the deadline.
- **Fallback ladder, each step coherent and wearable:** B with secondary screens off, then A, then A without motif lighting, then one hero screen with a printed static second module, then the sparse unlit crown.

Checkpoints from the manual stand: if the two-TFT bench stack is unstable, freeze at one hero screen; if fork diffusion needs too many LEDs, simplify geometry before adding power; if head-mounted power is uncomfortable, move power to the belt; if B compromises wearability, keep B as a belt display or sculpture.

## 4. Requirements

Thresholds marked TBD are not yet decided. They are listed so they get a number before CAD freezes, not invented here.

| ID | Requirement | Threshold | Verify | Status |
|----|-------------|-----------|--------|--------|
| REQ-001 | Comfortable timed wear | 30 minutes, no sharp edges, hot spots or cable pressure | 30-minute wear test | Open |
| REQ-002 | Fork lighting, both hero screens and master power run with no exposed wiring | Pass/fail | Inspection | Open |
| REQ-003 | Battery and controller cartridges removable without damaging finished surfaces | Pass/fail | Service test | Open |
| REQ-004 | Any screen cartridge replaceable independently | Pass/fail | Swap test (coupon M4) | Open |
| REQ-005 | Breakaway belt connection separates under a deliberate pull without stressing crown wiring | Pull force TBD | Snag test with helper | Open |
| REQ-006 | Design A stays visually finished with motif lighting omitted | Pass/fail | Visual review | Open |
| REQ-007 | Design B usable with secondary screens disabled | Pass/fail | Bench test | Open |
| REQ-008 | Crown mass | TBD (set from weighted dummy tests, coupon M5) | Scale, wear test | Open |
| REQ-009 | Runtime on one battery | TBD | Runtime test | Open |
| REQ-010 | Surface and connector temperature in enclosed operation | TBD | Thermal test | Open |
| REQ-011 | Donning and doffing time, and emergency removal | TBD | Timed trial | Open |
| REQ-012 | Fit: 607 mm head circumference at the crown track (confirmed by Brian), liner allowance, crown tilt, maximum height | Liner, tilt, height TBD | Fit-band print | Prov. locked (circumference only) |
| REQ-013 | Predictable restart into a safe scene after power loss | Pass/fail | Recovery test | Open |
| REQ-014 | Hero screens do not overwhelm the fork's visual dominance | Judgment review at several distances | Validation (experience), not verification | Open |

## 5. Interfaces and open decisions

The Universal Module Study v0.1 locks the principle (MOD-001) and keeps every dimension and pin provisional.

| ID | Decision | Maturity | Evidence |
|----|----------|----------|----------|
| MOD-001 | Universal module architecture: common receiver and power/signal connection; TV, phone, motif, light and blank modules interchangeable; identical carrier for TV and phone; decorative plugs are finished modules; retention independent of the electrical connector | Locked | ASM |
| IF-01 | Keyed slide or short dovetail plus positive latch for retention; magnets as registration aid only | Preferred | ASM |
| IF-02 | Shared power and SPI backbone, position-addressed stations, manual configuration first, pins reserved for module ID | Preferred | ASM |
| IF-03 | Dock face envelope, about 52 to 58 mm wide by 58 to 68 mm high; electronics depth 10 to 16 mm | Open (study values only) | ASM |
| IF-04 | Connector family, blind-mate versus cable lead, station count, current rating | Open | none |
| IF-05 | Front fork is a specialized hero subsystem, outside the universal dock | Preferred | ASM |
| IF-06 | Rear electronics and power-entry may use a larger service interface | Preferred | ASM |
| IF-07 | Mechanically design for B, electrically populate A | Locked | ASM |
| PWR-01 | Power: protected commercial USB pack first; belt pack with fuse or PTC at the source and a keyed magnetic breakaway is an option; no loose Li-ion/LiPo on the head | Preferred | ASM |
| MCU-01 | ESP32-S3, 240 x 320 ST7789 TFTs, identical displays preferred; buy and measure one TFT and one controller before bulk order | Prov. locked (procurement gate) | SPEC |

## 6. Evidence needed before interface lock

Measured TFT and controller dimensions and connector positions; fit-band print with liner and tilt; weighted dummy modules for mass and balance; fork lighting coupon (LED spacing and diffuser thickness by test, not rendering); insertion-cycle and signal-integrity tests; current and temperature under load; a consistent orthographic reference set of the chosen crown.

## 7. Top risks

| ID | Risk | Mitigation |
|----|------|------------|
| RSK-01 | Schedule: eleven days if the event is 31 October, with hardware not yet bought | Work the fallback ladder from the bottom; order one TFT and one controller now |
| RSK-02 | Two-TFT SPI stack unstable at wearable harness length | Desk test first; checkpoint 1 |
| RSK-03 | Head-mounted mass or heat causes discomfort | Weighted dummies; belt power option |
| RSK-04 | Magnetic breakaway contact rating or temperature | Measure under load before wear; source-side fuse |
| RSK-05 | Generated imagery mistaken for dimensional truth | Evidence tags; quarantine hardware details until verified |
| RSK-06 | Parallel chats drift on shared interfaces | Change-control rule (section 9) |

## 8. Workstreams

Chats 00 to 07 per the Setup Guide. Work is non-linear by design: any workstream can start at any time. What changes is its footing. A chat opened before its inputs are firm works against Open and Preferred items, labels every assumption with its maturity and evidence tag, and logs what it depends on, so later decisions can be traced.

| Chat | Title | Owns |
|------|-------|------|
| 00 | Design Director & Source of Truth | This brief, change requests, final approvals, reference views |
| 01 | CAD & Parametric Architecture | Head fit, skeleton, fork, spires, cartridge interfaces, sectors |
| 02 | Electronics, Power & Wiring | TFTs, ESP32 boards, LEDs, belt pack, breakaway, harness, schematics |
| 03 | Firmware, Media & Lighting | Drivers, asset pipeline, scenes, LED control, diagnostics |
| 04 | Fabrication, Assembly & Finish | Print settings, materials, fasteners, diffusion, paint, weathering |
| 05 | Belt & Costume Integration | Belt, power-pack housing, veil cable route, jacket, turtleneck |
| 06 | Build, Test & Revision Log | Prints, measurements, defects, current, heat, weight, fit |
| 07 | HFS Concept-to-Artifact Extraction | Reusable principles and HFS linkage (section 10) |

Authoritative artifacts: this brief (00); Build Manual (00, shared); Interface Control Document (01 + 02); CAD master assembly (01); schematic and pin map (02); firmware repository (03); fabrication traveler (04); Build and Test Log (06); HFS module seed (07). Crown documents stay separate from HFS methodology documents.

## 9. Change control

Subsystem chats do not silently alter shared interfaces or locked items. A change request goes to Chat 00 with: CR ID and date, originating workstream, current value, proposed value, reason and evidence, affected CAD/electronics/firmware/costume/docs, time and cost impact, decision (Approved, Rejected, Deferred), artifacts updated with revision numbers. Open and Preferred items can be changed by the owning chat with a one-line log entry; Prov. locked and Locked need a CR.

## 10. HFS linkage

This project is a test case for HFS and a source of HFS elements. Linkage runs both ways:

- **HFS informs the crown.** Each significant decision is checked against current HFS state (decision log, taxonomy, environment and operating-model documents, file-location rules).
- **The crown informs HFS.** Every decision gets an HFS note: followed, diverged, or new. Divergences get a Divergence Record: what HFS says, what we did, why, evidence, and the proposed HFS outcome (no change, clarify, amend, new pattern).
- **Where it runs.** Proposed: the crown is a Fabrication Incubator activity whose evidence feeds the Design Process. Chat 07 owns extraction; the Divergence and Extraction logs live with this brief; HFS check-ins pick them up.
- **Known candidates now.** (1) Fusion: HFS notes the free personal licence does not allow selling designs; Brian is modeling in Fusion. Fine for a personal costume, but it matters if crown CAD becomes an HFS module or product. (2) Naming: the Build Manual still says "Home Fab Studio"; HFS has conformed to "Home Fab System." (3) ID scheme: HFS uses COMPONENT-DOMAIN-TYPE-NNN; this brief uses project-local IDs (DG-, REQ-, IF-, RSK-) until a mapping is agreed. (4) Document mastering: HFS rules put one master per document in the hfs repository; where crown documents are mastered is open.

## 11. Open questions for Brian

1. Is the event date 31 October, and is anything else fixed?
2. Should the crown be filed as a Fabrication Incubator activity?
3. Where should the crown documents be mastered (this project, Drive, the hfs repo)?
4. Which REQ thresholds do you want to set now (mass, runtime, temperature, breakaway force)?
5. Is the Fusion question worth a Divergence Record now or only if the CAD is reused?

## Revision log

- v0.1 (2026-10-20): first draft from existing documents and chat decisions.

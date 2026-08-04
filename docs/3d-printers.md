# 3D Printers

We run a small fleet of Original Prusa FFF (filament) printers, each dedicated to a specific material family, plus a resin printer arriving later. Pick your printer by material first (PLA/PETG vs. flexible TPU vs. abrasive carbon-fiber/nylon composites need different machines), then by size (the XL's larger, multi-tool bed vs. the Core One's single-tool bed). All FFF machines currently run **0.4mm nozzles** and **Prusament-brand filament only** — see the [Prusa Slicer](#prusa-slicer) section below for why that matters and how to pick the right settings.

## Machines

### Prusa Core One (PLA/PETG)

**Location:** _[where in the shop]_
**Training required:** _[yes/no — sign-off process]_

**Overview**
A Prusa Core One — Prusa's enclosed, CoreXY FFF printer — dedicated to PLA and PETG. It uses the Nextruder hotend with an integrated loadcell sensor, which taps the bed to automatically set the first-layer height and mesh-level the bed before every print, so manual first-layer calibration generally isn't needed. This machine is the default choice for most general-purpose parts, prototypes, jigs, and anything that doesn't specifically need a flexible or engineering-grade material.

**Key Specifications**

| Spec | Value |
|---|---|
| Build volume | _[confirm — Core One is roughly 250 x 220 x 270 mm class; verify exact figure]_ |
| Materials supported | PLA, PETG (Prusament only — see Software section) |
| Nozzle size | 0.4mm (standard brass/CHT nozzle) |
| Slicer | Prusa Slicer |

**Basic Operating Steps**

1. Check in on the Fabman terminal at the printer to power it on.
2. From the printer's touchscreen, load filament through the built-in wizard if it's not already loaded (this preheats the nozzle and purges the old color/material automatically).
3. Slice your model in Prusa Slicer using the Core One (PLA/PETG) printer profile and the correct Prusament filament profile, then send the job via Prusa Connect or transfer it locally (see [Prusa Slicer](#prusa-slicer) below).
4. Start the print from the touchscreen; the printer will home and run its automatic bed-leveling/first-layer calibration before printing starts — watch the first layer go down before walking away.
5. When the print finishes, let the bed cool before removing the part (PETG in particular can warp/stick if forced off while still warm), clear any brim/skirt debris, and check out on the Fabman terminal.

**Manuals & Resources**

- [Prusa CORE One+ Knowledge Base](https://help.prusa3d.com/product/core-one-plus)
- [ ] Internal SOP / checklist (link)

---

### Prusa Core One (TPU)

**Location:** _[where in the shop]_
**Training required:** _[yes/no — sign-off process]_

**Overview**
A second Core One, dedicated entirely to flexible filament (TPU). Flexible filament is kept on its own machine rather than shared with the PLA/PETG unit because TPU needs a very different, much slower/gentler extrusion setup (flexible filament will buckle or jam in a feed path tuned for rigid filament), and because leftover TPU residue in a hotend/extruder can cause problems when switching back to a rigid material. *[NEEDS VERIFICATION: not yet set up as of this writing — confirm final specs once installed.]*

**Key Specifications**

| Spec | Value |
|---|---|
| Build volume | _[confirm]_ |
| Materials supported | TPU (Prusament only — see Software section) |
| Nozzle size | 0.4mm |
| Slicer | Prusa Slicer |

**Basic Operating Steps**

1. _[likely mirrors the PLA/PETG Core One workflow above — confirm once set up, especially TPU-specific load/purge steps]_
2.
3.

**Manuals & Resources**

- [Prusa CORE One+ Knowledge Base](https://help.prusa3d.com/product/core-one-plus)
- [ ] Internal SOP / checklist (link)

---

### Prusa Core One (Carbon Fiber/Nylon)

**Location:** _[where in the shop]_
**Training required:** _[yes/no — sign-off process, note abrasive-filament nozzle requirements]_

**Overview**
A third Core One, dedicated to carbon-fiber-filled and nylon filaments. Carbon-fiber-filled filament is highly abrasive and wears down a standard brass nozzle quickly, so this machine needs a **hardened (steel/tool-steel) nozzle** rather than the standard brass one — that's the main reason it's kept as its own dedicated machine rather than a swap-in profile on the PLA/PETG unit. Nylon is also hygroscopic (absorbs moisture from the air) and needs to be kept dry and printed promptly once opened. *[NEEDS VERIFICATION: not yet set up as of this writing — confirm final specs, and confirm the hardened nozzle is installed before running any carbon-fiber filament.]*

**Key Specifications**

| Spec | Value |
|---|---|
| Build volume | _[confirm]_ |
| Materials supported | Carbon-fiber-filled composites, Nylon (Prusament only — see Software section) |
| Nozzle | 0.4mm, hardened/wear-resistant — *[confirm nozzle material is actually hardened steel before running CF filament]* |
| Slicer | Prusa Slicer |

**Basic Operating Steps**

1. _[likely mirrors the PLA/PETG Core One workflow above — confirm once set up, especially nylon drying requirements before printing]_
2.
3.

**Manuals & Resources**

- [Prusa CORE One+ Knowledge Base](https://help.prusa3d.com/product/core-one-plus)
- [ ] Internal SOP / checklist (link)

---

### Prusa XL

**Location:** _[where in the shop]_
**Training required:** _[yes/no — sign-off process]_

**Overview**
The Prusa XL is a larger, CoreXY printer that supports up to **5 independent tool heads** on the same gantry, each with its own Nextruder (loadcell-based auto bed leveling/first-layer calibration) and its own 0.4mm nozzle. Because each tool has its own dedicated hot end, you can assign different materials to different tools without cross-contamination and, for jobs where the parts/zones don't touch, without needing a purge tower — this makes it well suited to larger single parts, batches of multiple parts in one job (optionally in different materials/colors per part), or anything too big for a Core One's bed. Use the XL over a Core One primarily for size, or for jobs that benefit from multiple tools in one run.

**Key Specifications**

| Spec | Value |
|---|---|
| Build volume | 360 x 360 x 360 mm |
| Tool heads | Up to 5 independent tool heads, automatic tool-change on the CoreXY gantry |
| Materials supported | _[confirm which materials/tools are currently loaded — Prusament only, per shop policy]_ |
| Nozzle size | 0.4mm per tool head |
| Slicer | Prusa Slicer |

**Basic Operating Steps**

1. Check in on the Fabman terminal at the printer to power it on.
2. Load filament into each tool head you plan to use via the touchscreen wizard (each tool loads independently).
3. Slice your model in Prusa Slicer using the Prusa XL printer profile (select the correct tool-count/nozzle configuration) and assign each object/part to the correct tool and Prusament filament profile, then send the job via Prusa Connect or transfer it locally (see [Prusa Slicer](#prusa-slicer) below).
4. Start the print; the machine will home, calibrate each active tool, and begin — watch the first layer and first tool change before walking away.
5. When finished, remove parts once the bed has cooled, and check out on the Fabman terminal.

**Manuals & Resources**

- [Using the printer — Original Prusa XL (Knowledge Base)](https://help.prusa3d.com/product/xl/using-the-printer_202)
- [Tools Mapping and Filament Mapping (XL, MMU3)](https://help.prusa3d.com/article/tools-mapping-and-filament-mapping-xl-mmu3_732461)
- [ ] Internal SOP / checklist (link)

---

### Prusa SLS Speed

!!! warning "Naming check"
    Prusa doesn't make an SLS (powder/laser-sintering) printer — their resin machine is the **Original Prusa SL1S SPEED**, an MSLA (LCD/UV resin) printer. This entry assumes that's the machine meant; if an actual powder-based SLS printer from another manufacturer is planned instead, most of the specifics below (resin, IPA wash, UV cure) won't apply and this section should be rewritten around that machine instead.

**Location:** _[where in the shop — not yet set up as of this writing]_
**Training required:** Yes — resin printing has a completely different hazard profile from FFF (liquid photopolymer resin, isopropyl alcohol for washing, UV curing) and needs its own safety training beyond general 3D printer sign-off.

**Overview**
The SL1S SPEED is an MSLA (masked stereolithography) resin printer: a high-resolution monochrome LCD panel masks a UV LED array to cure a photopolymer resin layer by layer, upside-down out of a resin vat. It is not a filament printer — there's no nozzle, no filament, and no Prusament FFF spool involved. Prints come off the printer needing to be washed (typically in isopropyl alcohol) and then UV-cured before they're usable. Because of this, it will need its own dedicated setup: resin storage/handling area, IPA wash station, curing station, and PPE (gloves, eye protection) separate from the FFF printers above.

**Key Specifications**

| Spec | Value |
|---|---|
| Build volume | _[confirm]_ |
| Technology | MSLA (LCD-masked UV resin curing), 405nm resin |
| Material | UV-curable photopolymer resin (Prusament Resin or compatible 405nm resin) |
| Post-processing needed | IPA wash + UV cure (not powder removal — see naming note above) |

**Basic Operating Steps**

1. _[not yet set up — steps to be confirmed once installed; general MSLA pattern is: prepare/shake resin, pour into vat, level/attach build plate, slice and send the job, run the print, then wash the part in IPA and UV-cure it before handling further]_
2.
3.

**Manuals & Resources**

- [Using the printer — Original Prusa SL1S SPEED (Knowledge Base)](https://help.prusa3d.com/product/sl1s-speed/using-the-printer_202)
- [Material guide — Original Prusa SL1S SPEED](https://help.prusa3d.com/product/sl1s-speed/material-guide_220)
- [ ] Internal SOP / checklist (link)

## Software

### Fusion (Design/CAD)

**Used for:** 3D modeling prior to slicing.
**Access:** _[license notes]_

**Basic Workflow**
Model your part, then export it for Prusa Slicer as either **STL** (a mesh — the most universal option, works everywhere) or **STEP** (a precise CAD solid; Prusa Slicer has supported importing STEP files natively since version 2.5, converting them to a mesh on import). STEP is worth using if you want to resize or make small tweaks without re-exporting from Fusion, since it preserves exact geometry rather than a fixed mesh — just know that very curved/filleted surfaces may need Prusa Slicer's import resolution turned up to look right. For most simple parts, STL is simpler and just as good.

**Resources**

- [ ] Getting-started guide (link)

---

### SolidWorks

**Used for:** 3D modeling prior to slicing, especially for more mechanical/engineering parts.
**Access:** _[license notes]_

**Basic Workflow**
Same export guidance as Fusion above: export **STL** (mesh, universal) or **STEP** (precise solid, natively importable in Prusa Slicer since 2.5) depending on whether you need to keep editing dimensions later.

**Resources**

- [ ] Getting-started guide (link)

---

### Prusa Slicer

**Used for:** Slicing models for every printer above, selecting the correct printer/nozzle/filament profile, and sending finished jobs to the shop's printers over Prusa Connect.
**Access:** Free — [download for Windows/macOS/Linux](https://www.prusa3d.com/page/prusaslicer_424/).

**Getting your file in**

Import your **STL** or **STEP** file (File → Import). STEP files are tessellated into a mesh on import — if curved surfaces look faceted, increase the import resolution and re-import. If you're picking up a project you or someone else already sliced, `.3mf` project files preserve object placement, per-object settings, and multi-part/multi-material assignments, which STL/STEP alone don't.

**Choosing the right printer profile**

Each physical printer in the shop is a separate profile/preset in Prusa Slicer (e.g. "Core One PLA/PETG", "Core One TPU", "Core One CF/Nylon", "Prusa XL") — pick the one that matches the machine and nozzle you're actually going to print on. All of them are currently configured for a **0.4mm nozzle**; if that ever changes on a given machine, the profile needs to be updated to match (extrusion width and layer height are both derived from nozzle size, so a mismatched profile will give bad results even if the file looks fine in the preview).

**Choosing the right filament profile**

We only stock **Prusament** filament, specifically because PrusaSlicer ships with verified, pre-tuned profiles for it (temperatures, cooling, flow, retraction) rather than the generic guesses used for unknown third-party filament — using the matching Prusament profile is how we get consistently good prints without members needing to tune settings by hand. To pick it:

1. Open the filament dropdown (or run the Configuration Wizard → Filaments tab) and select the **Prusament** vendor.
2. Choose the profile matching your material and the machine you're using — e.g. Prusament PLA, Prusament PETG, Prusament TPU, Prusament nylon/CF blends — matched to whichever Core One or XL tool is loaded with that material.
3. If a filament profile shows up with a red flag, it's marked incompatible with your current printer/nozzle profile — don't use it. Double-check you've selected the right printer profile first; a red flag is usually a sign the printer and filament profiles don't agree on nozzle size or printer model.

**Connecting to a printer over Prusa Connect**

Each printer only powers on when someone checks in at its Fabman terminal — sending a job from home or before checking in will fail because the printer has no power. Once you're at the shop and checked in on the correct machine's Fabman terminal:

1. In Prusa Slicer, go to **File → Printer Settings**, and make sure the base printer profile matches the machine you're using.
2. Under **Physical Printer → Add physical printer**, give it a clear name (e.g. `Makerspace Core One PLA-PETG`), set **Host Type** to `PrusaConnect`, and leave the Hostname/IP/URL field at its auto-filled default.
3. Enter that printer's **API Key**. Each physical printer has its own key — ask a shop lead for the current key for the machine you're using (these are intentionally not published in this wiki since it's public; keep them in the shop's internal/restricted reference instead).
4. Click **Test** to confirm Prusa Slicer can reach the printer — this only succeeds if you've checked in on that printer's Fabman terminal and it's powered on.
5. Slice your model, then instead of exporting G-code to a file, choose **Send to printer** (or pick the physical printer from the dropdown at the top of the window). Confirm the send — the job uploads to Prusa Connect and appears in the printer's queue.
6. Walk to the printer and start the print from its touchscreen (or confirm it starts automatically, depending on the printer's settings).
7. When you're done, check out on the same Fabman terminal — this logs your usage time and powers the printer down.

!!! warning "Troubleshooting"
    - **"Could not connect" / test fails:** the printer is powered off — check in on its Fabman terminal first.
    - **API key rejected:** double-check for extra spaces when pasting the key.
    - **Print sent but printer shows nothing:** it may still be booting after Fabman check-in — wait ~30 seconds and refresh.
    - **Need to track your usage time:** make sure you checked in **and** checked out on the Fabman terminal — Fabman logs your hours from that session, not from Prusa Slicer.

**Resources**

- [PrusaSlicer download](https://www.prusa3d.com/page/prusaslicer_424/)
- [Prusa Connect and PrusaLink explained](https://help.prusa3d.com/article/prusa-connect-and-prusalink-explained_1)
- [Adding the printer to Prusa Connect](https://help.prusa3d.com/article/adding-the-printer-to-prusa-connect-core-one-mk4-s-mk3-9-s-mk3-5-s-xl-mini_1)

## Safety

!!! danger "Required before first use"
    _[Certification/training requirement per machine — the resin printer (SL1S SPEED) in particular needs separate safety training beyond the FFF printers' sign-off, covering resin handling, IPA use, and UV curing.]_

- **PPE:** Burn awareness around hot nozzles/beds on all FFF machines (Core Ones, XL). For the resin printer once installed: nitrile gloves and eye protection are required any time you're handling uncured resin or IPA.
- **Ventilation:** Materials like nylon and ABS/ASA off-gas more than PLA — print them with reasonable ventilation. Resin printing (once set up) needs its own ventilated area due to fumes from uncured resin and IPA.
- **Never leave a print unattended overnight without approval:** _[shop policy]_
- **Nozzle handling:** Don't touch the nozzle or bed shortly after a print finishes — both stay hot well after printing stops.
- **Resin handling (SL1S SPEED, once set up):** Uncured resin is a skin irritant — avoid contact, clean spills promptly, and dispose of used IPA and cured resin waste per local regulations, not down the drain.
- **Emergency procedures:** _[who to contact, incident reporting process]_

## FAQ

**Q: Which printer should I use for my part?**
A: Start from the material you need: PLA or PETG → Core One (PLA/PETG); flexible parts → Core One (TPU); carbon-fiber-reinforced or nylon parts → Core One (CF/Nylon); a part too large for a Core One's bed, or a job with multiple parts/materials in one run → Prusa XL. High-detail, small, or resin-only parts will eventually go on the SL1S SPEED once it's set up.

**Q: Do I need to bring my own filament/material?**
A: No — the shop only runs Prusament filament on these printers, since Prusa Slicer's verified Prusament profiles are what gets consistently good results without manual tuning. Bringing third-party filament isn't supported on the shop printers under current policy. *[NEEDS VERIFICATION: confirm this is the actual shop policy, and whether members can request a specific Prusament material be stocked.]*

**Q: How do I reserve print time?**
A: _[NEEDS VERIFICATION — likely via the Fabman check-in system, possibly combined with a booking/queue tool; confirm the actual process.]_

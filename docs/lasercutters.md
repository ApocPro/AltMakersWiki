# Laser Cutters

The laser cutting area is for engraving and cutting thin, flat sheet materials (wood, acrylic, leather, cardboard, etc.) using a focused laser beam controlled through Lightburn software. Use a laser cutter when you need clean, precise 2D cuts or surface engraving on flat stock within the machine's thickness limit; use the CNC router instead for thicker stock, 3D shaping, or materials that aren't laser-safe. *[NEEDS VERIFICATION: confirm this laser-vs-CNC guidance with a shop lead.]*

## Machines

### Monport Effi 16s

**Location:** _[NEEDS VERIFICATION — where in the shop]_
**Training required:** Yes. Access to the shared Lightburn workstation currently uses a shared login (`alt-makers-2026`). *[NEEDS VERIFICATION: confirm whether a separate certification/sign-off is required beyond this login, and whether this credential should live in a restricted document rather than a public wiki page.]*

**Overview**
The Effi 16s is a 150W CO2 laser engraver/cutter with a built-in water chiller and autofocus. It has a roughly 1.6m x 1m working bed and is the primary machine covered in our internal training walkthrough. It's controlled through Lightburn and uses a physical keypad on the machine for jogging, focusing, and starting jobs.

**Key Specifications**

| Spec | Value |
|---|---|
| Bed size | ~1600 x 1000 mm (1.6 m x 1 m) |
| Laser type/power | CO2, 150W (rated; peak up to ~180W) |
| Max material thickness | 5mm MDF cuts through in a single pass at tested settings below; thicker material may need multiple passes with Z-offset between passes. *[NEEDS VERIFICATION: confirm the machine's published max cut depth per material.]* |
| Software/controller | Lightburn (front-end); onboard digital control panel/keypad for jogging, focus, and start *[NEEDS VERIFICATION: confirm controller brand, e.g. Ruida]* |

**Basic Operating Steps**

1. Design or import your artwork in Lightburn (see [Lightburn workflow](#lightburn) below) and set up your cut/engrave layers.
2. Open the lid, then power on the machine (twist/release the emergency-stop switch); the laser head will home to the back-right corner — make sure nothing is in its path first.
3. Load your material, adjust bed height for material thickness, jog the laser over the material, and run autofocus.
4. Frame the job to confirm it fits on your material, confirm the exhaust/air filter is running, close the lid, and press Start on the machine.
5. Wait for the job to finish without opening the lid (opening the lid mid-job immediately stops the laser, and jobs cannot resume from where they left off).

**Manuals & Resources**

- [ ] [Monport Effi16S product/spec page](https://monportlaser.com/products/monport-effi16s-upgraded-150w-co2-laser-engraver-cutter-with-autofocus-and-built-in-water-chiller)
- [ ] [Monport Effi16S manuals (ManualsLib)](https://www.manualslib.com/products/Monport-Effi16s-14512154.html)
- [ ] Internal SOP / checklist (link) — *[NEEDS VERIFICATION: not yet created]*

---

### Monport Mega

**Location:** _[NEEDS VERIFICATION — where in the shop]_
**Training required:** _[NEEDS VERIFICATION — yes/no, link to sign-off form]_

**Overview**
The Mega is a smaller desktop 70W CO2 laser, meant for smaller jobs or as a second machine when the Effi 16s is in use. It has a smaller bed and lower power than the Effi 16s, so it's better suited to smaller or lower-power engraving/cutting jobs rather than large sheet work. *[NEEDS VERIFICATION: this comparison is inferred from published specs, not from the training transcript — confirm with a shop lead which jobs should default to the Mega vs. the Effi 16s.]*

**Key Specifications**

| Spec | Value |
|---|---|
| Bed size | ~700–780 x 400–440 mm *[NEEDS VERIFICATION: exact bed size varies by Mega/Mega S listing — confirm on the physical unit]* |
| Laser type/power | CO2, 70W |
| Max material thickness | _[NEEDS VERIFICATION]_ |
| Software/controller | Lightburn |

**Basic Operating Steps**

1. _[NEEDS VERIFICATION — likely mirrors the Effi 16s workflow below, but confirm keypad/homing differences]_
2. 
3. 

**Manuals & Resources**

- [ ] [Monport Mega product page](https://monportlaser.com/products/monport-mega-the-worlds-premier-70w-intelligent-desktop-engraving-machine)
- [ ] Internal SOP / checklist (link) — *[NEEDS VERIFICATION: not yet created]*

## Software

### Lightburn

**Used for:** Primary laser control software for both machines — importing/designing artwork, tracing images into vector lines, assigning cut/engrave settings by layer, previewing the job, and running it on the machine.
**Access:** Shared workstation login: `alt-makers-2026`. *[NEEDS VERIFICATION: confirm license seat/install details, and whether this login should be kept in an access-restricted doc instead of a public wiki.]*

**Basic Workflow**

1. **Import your design.** File → Import (or drag and drop) — almost any image format works (PNG, JPG, SVG, etc.). You no longer need a pre-made vector file to get started.
2. **Trace the image (if it's not already a vector).** Select the imported image, then Tools → Trace Image. Lightburn previews the traced outline as a purple line — adjust the threshold sliders if the trace looks wrong, but the default is usually fine. Once you're happy, confirm, and you can delete or hide the original image layer since Lightburn now has vector lines to work with.
3. **Assign layers in the Cuts/Layers panel** (right-hand side tabs: Move, Cuts/Layers, Camera, Variable Text — it opens on Move by default, switch to Cuts/Layers). For each layer you can set:
   - **Output** — on/off switch for whether that layer fires at all when you run the job.
   - **Mode** — Line (outline only), Fill (solid engrave inside the line), or Offset Fill (fills everything *outside* the line).
   - **Air** — whether air assist runs for that layer.
   - Double-click a layer to open Speed/Power settings (stay in the "Common" tab — you generally don't need the advanced tab): speed, min/max power, number of passes, line interval, and Bidirectional / Unidirectional / Crosshatch fill direction.
   - Layer order (top to bottom in the list) is the order operations run in — always put engraving layers above cutting layers, since cutting can shift or dislodge your material before an engrave finishes. Layer *color* has no functional meaning; it's just for your own organization.
4. **Position and size your design.** Use the top toolbar to set exact width/height (linked or independent), rotate by a typed angle, or scale by percentage (note: after typing a percentage, the field resets to "100%" — remember your last adjustment, or use Undo/Cmd+Z). You can also change which reference point (corner/center) the X/Y position refers to. Holding Ctrl while dragging snaps rotation to ~5° increments; holding Shift snaps to ~15° increments. *[NEEDS VERIFICATION: confirm these snap increments against the installed Lightburn version — they can vary slightly.]*
   - The machine's absolute (0,0) origin is the back-right corner (where the laser homes to on power-up) — not every laser uses this corner, so don't assume based on other machines.
5. **Draw extra shapes if needed** (e.g., a cut outline around an engraved design) using Lightburn's built-in shape tools, and assign them to their own layer (e.g., layer 2 for cuts). To round sharp corners: select the shape, click a corner node, then use the corner-rounding control in the bottom-left panel and set a radius; click the node again to undo the rounding.
6. **Set your job origin.** Under laser controls, "Start From" can be set to Absolute Coordinates (travels to a specific point on the bed — useful when filling the entire bed) or Current Position (starts wherever the laser head currently is — useful for smaller jobs, since you just jog the head to a corner of your material first).
7. **Frame the job before cutting.** With your design selected, use the square Frame button for roughly rectangular designs, or the circular "rubber band" frame for irregular shapes — this traces the job's bounding area on the material at a safe (non-cutting) speed so you can confirm it fits and is positioned correctly.
8. **Preview the toolpath** using the monitor icon in the top toolbar: black lines mean the laser fires (cutting or engraving), red lines are travel moves with the laser off.
9. **Run the job** on the machine's physical keypad once framing looks correct, the exhaust/filter is running, and the lid is closed.

**Resources**

- [ ] [LightBurn documentation home](https://docs.lightburnsoftware.com/)
- [ ] [LightBurn: Tracing Images](https://docs.lightburnsoftware.com/Tools/TracingImages.html)

---

### Inkscape

**Used for:** Optional vector design/cleanup before bringing artwork into Lightburn — useful if you want to build clean vector lines yourself rather than relying on Lightburn's image trace.
**Access:** Free, open source. *[NEEDS VERIFICATION: confirm install location/link for shop computers.]*

**Basic Workflow**
_[NEEDS VERIFICATION — not covered in the training transcript. General pattern: design or clean up vectors in Inkscape → export/save as SVG → import that SVG into Lightburn instead of tracing a raster image.]_

**Resources**

- [ ] Getting-started guide (link) — *[NEEDS VERIFICATION]*

## Materials

Only MDF (white) was actually tested and confirmed during training (3mm and 5mm thicknesses, settings below). Monport's own reference chart also lists Baltic birch, acrylic/plexiglass, and leather as compatible materials for this laser class, but these have **not** been locally tested/confirmed — check the Lightburn material library (being added — see note below) or get sign-off from a shop lead before using an untested material.

*[NEEDS VERIFICATION: the built-in Lightburn material library was not yet populated as of this training session — confirm it now has entries for Baltic birch, MDF, acrylic, and other approved materials, and update this table accordingly.]*

| Material | Max thickness | Notes |
|---|---|---|
| MDF (white) | 5mm (single pass) | Confirmed in training; see Tool Settings below |
| Baltic birch plywood | _[NEEDS VERIFICATION]_ | Listed in Monport's reference chart; not locally tested |
| Acrylic/plexiglass | _[NEEDS VERIFICATION]_ | Listed in Monport's reference chart; not locally tested |
| Leather | _[NEEDS VERIFICATION]_ | Listed in Monport's reference chart; not locally tested |

!!! danger "Never cut these materials"
    PVC/vinyl, ABS, polycarbonate, and other chlorinated or halogenated plastics — these release toxic chlorine gas/hydrochloric acid when laser-cut, even with ventilation running. Also avoid fiberglass, certain foams, HDPE, coniferous/oily woods, and any material of unknown composition. If you can't confirm what a material is made of, don't cut it — ask first.

## Tool Settings

The values below were arrived at live during training on the **Effi 16s (150W)**, cutting/engraving **white MDF**. Treat the cut setting as a working starting point, not a fully verified reference — the audio was unclear on a couple of numbers, and it was derived from Monport's Baltic-birch chart (converted from a quarter-inch imperial spec) rather than an MDF-specific value. Re-verify against the Lightburn material library once it's populated.

| Material | Thickness | Power | Speed | Passes | Notes |
|---|---|---|---|---|---|
| MDF (white) | — (engrave/fill) | 20% | 230 mm/s | 1 | Fill mode, bidirectional; air assist **off** (kept off deliberately to avoid blowing white MDF dust around — air assist for engraving is a matter of preference); line interval widened from Lightburn's 0.1mm default since this laser's focal spot is ~0.15mm (0.1mm default causes overlap) |
| MDF (white) | 3mm | 26% | 9 mm/s | 1 | Cut (Line mode); air assist **on** (required for all cuts) *[NEEDS VERIFICATION: exact speed/power heard as "9mm/s at 26%" from Monport's quarter-inch birch chart — confirm]* |
| MDF (white) | 5mm | 26% | 9 mm/s | 1 | Same quarter-inch-chart settings used for the 3mm cut were reused here to ensure full through-cut; confirm depth and consider dedicated MDF settings once available |

General notes:
- Engrave layers should always be ordered above cut layers, so engraving happens before the material can shift from cutting.
- Number of Passes = 1 is meant to cut all the way through in one go; for thicker material, increase passes and adjust the Z-focus offset down between passes rather than trying to increase power/reduce speed indefinitely.
- Bidirectional fill (laser fires moving both directions) is faster; unidirectional (fires one direction only) is slower but can look more consistent; crosshatch (do a pass each direction) gives more uniform/deeper engraves.

## Safety

!!! danger "Required before first use"
    _[NEEDS VERIFICATION: confirm the certification/training requirement and sign-off process — the transcript only mentions a shared Lightburn login (`alt-makers-2026`), not a formal certification step.]_

- **PPE:** Laser safety glasses rated for this laser's wavelength if operating with the lid open at any point; general good practice includes avoiding loose clothing/hair near the machine. *[NEEDS VERIFICATION]*
- **Ventilation/exhaust:** The exhaust/air filter must be confirmed running before closing the lid and starting any job — this was called out explicitly as a pre-start checklist item during training.
- **Fire safety:** Never leave the machine running unattended. A small amount of flame/smoke during cutting or engraving is normal (air assist blows it away from the beam path, and the fan pulls smoke out). If you see a large or sustained flame, open the lid immediately — this cuts power to the laser automatically, same as pressing emergency stop. Location of fire extinguisher: _[NEEDS VERIFICATION]_.
- **Material approval:** Always confirm a material is on the approved list (see Materials section) before cutting — never guess based on appearance.
- **Emergency stop:** Twisting/releasing the emergency-stop switch also powers the machine on; pressing it (or simply opening the lid at any time) immediately halts the laser. Exact physical location on each machine: _[NEEDS VERIFICATION]_.
- **Emergency procedures:** _[NEEDS VERIFICATION — who to contact, incident reporting process]_

## FAQ

**Q: How do I know if a material is safe to cut?**
A: Check the Materials list above and the Lightburn material library first. If it's not listed, don't assume it's fine — get approval from a shop lead before cutting. Unknown-composition materials (and anything containing PVC/vinyl, ABS, or other chlorinated plastics) are never safe to cut, regardless of ventilation.

**Q: What do I do if the laser doesn't fire / air assist doesn't turn on?**
A: Check that the layer's **Output** toggle is on in the Cuts/Layers panel, that the lid is fully closed (an open lid disables firing), and that the machine's power/interlock is engaged. *[NEEDS VERIFICATION: this troubleshooting wasn't directly covered in the training transcript — confirm steps and add air-assist-specific checks, e.g. compressor/air line connection.]*

**Q: Can I bring my own material?**
A: _[NEEDS VERIFICATION — not addressed in the training transcript. As a general safety rule, any new/outside material should be checked against the Materials list and approved before use, since the main risk with laser cutters is toxic fumes from unknown plastics.]_

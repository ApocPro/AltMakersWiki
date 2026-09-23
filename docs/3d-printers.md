# 3D Printers

We run Original Prusa FFF (filament) printers, each currently dedicated to a specific material family. We have ordered the INDX tool changer for 2 of the printers which will enable you to do multi material, multi color prints on 3 of the 4 printers that we have. Pick your printer by material first (PLA/PETG vs. flexible TPU vs. abrasive carbon-fiber/nylon composites need different machines), then by size (the XL's larger, multi-tool bed vs. the Core One's single-tool bed). All FFF machines currently run **0.4mm nozzles** and **Prusament-brand filament only** — see the [Prusa Slicer](#prusa-slicer) section below for why that matters and how to pick the right settings.

## Machines

### Prusa Core One (PLA/PETG)

**Location:** _Entrance, Left-hand side_
**Training required:** _yes_

**Overview**
A Prusa Core One — Prusa's enclosed, CoreXY FFF printer — dedicated to PLA and PETG. It uses the Nextruder hotend with an integrated loadcell sensor, which taps the bed to automatically set the first-layer height and mesh-level the bed before every print, so manual first-layer calibration generally isn't needed. This machine is the default choice for most general-purpose parts, prototypes, jigs, and anything that doesn't specifically need a flexible or engineering-grade material.

**Key Specifications**

| Spec | Value |
|---|---|
| Build volume | _250 x 220 x 270 mm_ |
| Materials supported | PLA, PETG (material provided, Prusament only) |
| Nozzle size | 0.4mm (standard brass/CHT nozzle) |
| Slicer | Prusa Slicer |

**Basic Operating Steps**

1. Turn the printer on from the back right side.
2. Check the build plate
 - Is the correct plate inserted?: Smooth: PLA only, never use PETG on the smooth plate ; Textured: best for PETG, PLA can be used; Satin: happy medium, best for both PLA and PETG
 - Is the build plate clean? No left over material in the corner, no fingerprints.
 - Is the build plate properly inserted?  Resting against the screws in the back, centered, name of the plate right-side up when you read it?
3. From the printer's touchscreen, change filament through the built-in wizard (or load if it's not already loaded) This preheats the nozzle and purges the old color/material automatically. Skip this step if you want to use the material that is already loaded.
4. Slice your model in Prusa Slicer using the _Prusa CORE One HF0.4 nozzle_ printer profile and the correct Prusament filament profile, then send the job via Prusa Connect. (You will have be added to the Prusa Connect Team after training so you can access the printers).
5. Start the print from Prusa Connect or the touchscreen; the printer will home and run its automatic bed-leveling/first-layer calibration before printing starts — watch the first layer go down before walking away.
5. When the print finishes, let the bed cool before removing the part (PETG in particular can warp/stick if forced off while still warm), clear any brim/skirt debris.

**Manuals & Resources**

- [Prusa CORE One+ Knowledge Base](https://help.prusa3d.com/product/core-one-plus)


---

### Prusa Core One (TPU)

**Location:** _under the table, still needs to be setup_
**Training required:** _yes_

**Overview**
A second Core One, dedicated entirely to flexible filament (TPU). Flexible filament is kept on its own machine rather than shared with the PLA/PETG unit because TPU needs a very different, much slower/gentler extrusion setup (flexible filament will buckle or jam in a feed path tuned for rigid filament), and because leftover TPU residue in a hotend/extruder can cause problems when switching back to a rigid material. Once we have the INDX setup, instead of having a separate printer for TPU, we will simply have dedicated nozzles for only TPU.

**Key Specifications**

| Spec | Value |
|---|---|
| Build volume | _250 x 220 x 270 mm_ |
| Materials supported | TPU (material provided, Prusament only) |
| Nozzle size | 0.4mm |
| Slicer | Prusa Slicer |

**Basic Operating Steps**

Same as the PLA/PETG printer, just make sure that you choose TPU in Prusa Slicer when you are slicing your model.

**Manuals & Resources**

- [Prusa CORE One+ Knowledge Base](https://help.prusa3d.com/product/core-one-plus)

---

### Prusa Core One (Carbon Fiber/Nylon)

**Location:** _under the table, still needs to be setup_
**Training required:** _yes_

**Overview**
A third Core One, dedicated to carbon-fiber-filled and nylon filaments. Carbon-fiber-filled filament is highly abrasive and wears down a standard brass nozzle quickly, so this machine has a **hardened ruby nozzle** rather than the standard brass one — that's the main reason it's kept as its own dedicated machine rather than a swap-in profile on the PLA/PETG unit. Nylon is also hygroscopic (absorbs moisture from the air) and needs to be kept dry and printed promptly once opened. Nylon is kept in a dedicated dry box.  Please do not open the box, the material will be feed directly from the box and a member of staff will replace it when needed.

**Key Specifications**

| Spec | Value |
|---|---|
| Build volume | _250 x 220 x 270 mm_ |
| Materials supported | Carbon-fiber-filled composites, Nylon (material provided) |
| Nozzle | 0.4mm, hardened/wear-resistant |
| Slicer | Prusa Slicer |

**Basic Operating Steps**

1. will be completed once the printer is set up

**Manuals & Resources**

- [Prusa CORE One+ Knowledge Base](https://help.prusa3d.com/product/core-one-plus)

---

### Prusa XL - 5T 

**Location:** _Entrance Right-side_
**Training required:** _yes_

**Overview**
The Prusa XL is a larger, CoreXY printer that supports **5 independent tool heads** on the same gantry, each with its own Nextruder (loadcell-based auto bed leveling/first-layer calibration) and its own 0.4mm nozzle. Because each tool has its own dedicated hot end, you can assign different materials to different tools without cross-contamination and, for jobs where the parts/zones don't touch, without needing a purge tower — this makes it well suited to larger single parts, batches of multiple parts in one job (optionally in different materials/colors per part), or anything too big for a Core One's bed. Use the XL over a Core One primarily for size, or for jobs that benefit from multiple tools in one run.

**Key Specifications**

| Spec | Value |
|---|---|
| Build volume | 360 x 360 x 360 mm |
| Tool heads | Up to 5 independent tool heads, automatic tool-change on the CoreXY gantry |
| Materials supported | _PLA and PETG (material provided, Prusament only)_ |
| Nozzle size | 0.4mm per tool head |
| Slicer | Prusa Slicer |

**Basic Operating Steps**

1. Turn the printer on from the back right side.
2. Check the build plate
 - Is the correct plate inserted?: Smooth: PLA only, never use PETG on the smooth plate ; Textured: best for PETG, PLA can be used; Satin: happy medium, best for both PLA and PETG
 - Is the build plate clean? No left over material in the corner, no fingerprints.
 - Is the build plate properly inserted?  Resting against the screws in the back, centered, name of the plate right-side up when you read it?
3. From the printer's touchscreen, change filament through the built-in wizard (or load if it's not already loaded) This preheats the nozzle and purges the old color/material automatically. Skip this step if you want to use the material that is already loaded. Each tool has it's own material spool, 1-3 are on the left, 4 and 5 are on the right.  The points where the material is inserted into the boden tube to go into the machine are numbered so you know what material is for what tool.
4. Slice your model in Prusa Slicer using the _Original Prusa XL - 5T Input Shaper 0.4 nozzle_ printer profile and the correct Prusament filament profile, then send the job via Prusa Connect. (You will have be added to the Prusa Connect Team after training so you can access the printers).
5. Start the print from Prusa Connect or the touchscreen; the printer will home and run its automatic bed-leveling/first-layer calibration before printing starts — watch the first layer go down before walking away.
5. When the print finishes, let the bed cool before removing the part (PETG in particular can warp/stick if forced off while still warm), clear any brim/skirt debris.

**Manuals & Resources**

- [Using the printer — Original Prusa XL (Knowledge Base)](https://help.prusa3d.com/product/xl/using-the-printer_202)
- [Tools Mapping and Filament Mapping (XL, MMU3)](https://help.prusa3d.com/article/tools-mapping-and-filament-mapping-xl-mmu3_732461)

---

## Software

### Fusion (Design/CAD)

**Used for:** 3D modeling prior to slicing.
**Access:** _fusion for personal use is free and allows you to use the full functionality of CAD as long as only 10 models are active at one time_

**Basic Workflow**
Model your part, then export it using the Utilites menu: MAKE -> 3D Print
In the 3D Print Dialogue, choose the following:
- Preparation Type: Print Utility
- Application: Prusa Slicer
- Object: _chose the object from your design that you want to print_
- Format: STL (Binary)
- Unit Type: _same as whatever you modeled, most likely millimeter_

**Resources**

- Youtube tutorials: Learn Autodesk Fusion in 30 Days https://www.youtube.com/watch?v=4G2E_DqQteM (great tutorials, you will understand everything that you need 99% of the time in the first 5 tutorials, but the other 25 are also great as you get more advanced)

---

### SolidWorks

**Used for:** 3D modeling prior to slicing, especially for more mechanical/engineering parts.
**Access:** _We have a makerspace license.  Ask us if you are interested and we can provide you access.  Solidworks works either online or natively on Windows devices._

**Basic Workflow**
Model your part, then export **STL** (mesh, universal) or **STEP** (precise solid, natively importable in Prusa Slicer since 2.5) depending on whether you need to keep editing dimensions later.
Solidworks is used and has been used for decades in Engineering CAD.  For this reason it is very powerful, but can be less intuitive when you are starting out

**Resources**

- Portal: https://eu1-makers.iam.3dexperience.3ds.com/login?serverId=FRONT_0_8089&service=https%3A//eu1-makers-ifwe.3dexperience.3ds.com/

---

### Prusa Slicer

**Used for:** Slicing models for every printer above, selecting the correct printer/nozzle/filament profile, and sending finished jobs to the shop's printers over Prusa Connect.
**Access:** Free — [download for Windows/macOS/Linux](https://www.prusa3d.com/page/prusaslicer_424/).

**Getting your file in**

Import your **STL** or **STEP** file (File → Import). STEP files are tessellated into a mesh on import — if curved surfaces look faceted, increase the import resolution and re-import. If you're picking up a project you or someone else already sliced, `.3mf` project files preserve object placement, per-object settings, and multi-part/multi-material assignments, which STL/STEP alone don't.

**Choosing the right printer profile**

Each physical printer in the shop is a separate profile/preset in Prusa Slicer (e.g. _Prusa CORE One HF0.4 nozzle_, _Original Prusa XL - 5T Input Shaper 0.4 nozzle_ ) — pick the one that matches the machine and nozzle you're actually going to print on. All of them are currently configured for a **0.4mm nozzle**; if that ever changes on a given machine, the profile needs to be updated to match (extrusion width and layer height are both derived from nozzle size, so a mismatched profile will give bad results even if the file looks fine in the preview).

**Choosing the right filament profile**

We only stock **Prusament** filament, specifically because PrusaSlicer ships with verified, pre-tuned profiles for it (temperatures, cooling, flow, retraction) rather than the generic guesses used for unknown third-party filament — using the matching Prusament profile is how we get consistently good prints without members needing to tune settings by hand. To pick it:

1. Open the filament dropdown (or run the Configuration Wizard → Filaments tab) and select the **Prusament** vendor.
2. Choose the profile matching your material and the machine you're using — e.g. Prusament PLA, Prusament PETG, Prusament TPU, Prusament nylon/CF blends — matched to whichever Core One or XL tool is loaded with that material.
3. If a filament profile shows up with a red flag, it's marked incompatible with your current printer/nozzle profile — don't use it. Double-check you've selected the right printer profile first; a red flag is usually a sign the printer and filament profiles don't agree on nozzle size or printer model.

**Connecting to a printer over Prusa Connect**

If the printer is on you can find it in Prusa Connect.  Do not start your print from home.  Even though you can see through the camera that the bed is clear, you are required to come in and go through the proper start proceedure to make sure that there is enough material loaded in the printer to complete your print and that everything is properly setup.  Starting your print completely remotely has too many risks that can cost you and/or the space money.

1. In Prusa Slicer, go to **File → Printer Settings**, and make sure the base printer profile matches the machine you're using. You can keep the standard System presets. You can make changes but please make sure you understand the changes you make before you assume that the printer will just run smoothly with whatever setting.
2. Under **Printers → Add/Remove printer**, go through the configuration wizard and choose _Prusa CORE One & One+ & One+ (Gen2) HF0.4 mm nozzle_ and _Original Prusa XL - 5T Input Shaper 0.4 mm nozzle_
3. This provides you with the correct settings for our printers so you can slice your design.  When you go to **Prusa Connect** You will see our actual printers: _Alt-MakersXL5_ and _PLA/PETG - CoreOne+_
4. Slice your model, then instead of exporting G-code to a file, choose **Send to Connect** and choose the correct printer. Confirm the send — the job uploads to Prusa Connect and appears in the printer's queue.
5. Walk to the printer and start the print from its touchscreen (or confirm it starts automatically, depending on the printer's settings).

!!! warning "Troubleshooting"
    - **"Could not connect" / test fails:** the printer is powered off or has failed to connect to the network, turn it off and on again
    - **Print sent but printer shows nothing:** it may still be loading — wait ~30 seconds. If nothing comes check the network connection in the touchscreen

**Resources**

- [PrusaSlicer download](https://www.prusa3d.com/page/prusaslicer_424/)
- [Prusa Connect and PrusaLink explained](https://help.prusa3d.com/article/prusa-connect-and-prusalink-explained_1)
- [Adding the printer to Prusa Connect](https://help.prusa3d.com/article/adding-the-printer-to-prusa-connect-core-one-mk4-s-mk3-9-s-mk3-5-s-xl-mini_1)

## Safety

!!! danger "Required before first use"

- **PPE:** Burn awareness around hot nozzles/beds on all FFF machines (Core Ones, XL). 
- **Ventilation:** Materials like nylon and ABS/ASA off-gas more than PLA — we do not print ABS or ASA because of this, the nylon printer will have dedicated ventilation. 
- **Printing overnight is allowed, but make sure the light in the machine is shut off in the Control Menu in Prusa Connect**
- **Nozzle handling:** Don't touch the nozzle or bed shortly after a print finishes — both stay hot well after printing stops.

## FAQ

**Q: Which printer should I use for my part?**
A: Start from the material you need: PLA or PETG → Core One (PLA/PETG); flexible parts → Core One (TPU); carbon-fiber-reinforced or nylon parts → Core One (CF/Nylon); a part too large for a Core One's bed, or a job with multiple parts/materials in one run → Prusa XL.

**Q: Do I need to bring my own filament/material?**
A: No — the shop only runs Prusament filament on these printers, since Prusa Slicer's verified Prusament profiles are what gets consistently good results without manual tuning. Bringing third-party filament isn't supported on the shop printers under current policy. 

**Q: How do I reserve print time?**
A: There is no "reservation". Instead there is a print queue.  If someone is using the printer, upload your print to the queue and once the printer is set to ready the next print in the queue can be started.

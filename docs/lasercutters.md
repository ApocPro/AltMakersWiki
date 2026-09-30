# Laser Cutters

The laser cutting area is for engraving and cutting thin, flat sheet materials (wood, acrylic, leather, cardboard, etc.) using a focused laser beam controlled through Lightburn software. Use a laser cutter when you need clean, precise 2D cuts or surface engraving on flat stock within the machine's thickness limit; use the CNC router instead for thicker stock, 3D shaping, or materials that aren't laser-safe. 

## Quick Start: Cutting on the Effi 16s

The full job, start to finish, in order. Each step links to the detailed section if you need more. This assumes you've done the laser training and your member chip is activated for the laser.

!!! warning "Three rules that protect you and the machine"
    - **Never raise the bed into the laser head.** Always lower first, then bring it up slowly.
    - **Never go above 70% power.** Higher power shortens the life of the laser tube (and it's expensive to replace).
    - **Never leave the machine while it's running.** You have to confirm you're there every two minutes, and no one else can do that for you unless they're a trained member.

### 1. Before you start

1. Check that your material is safe to cut. If it's not in the [settings library](lasercutters-material-settings-effi16s.md), or you're not sure what it's made of, check the [unsafe materials list](lasercutters-unsafe-materials-en.md) or ask. **No PVC/vinyl, ever.**
2. If the room is above 35 °C, don't use the laser. The chiller can't keep the tube cool.
3. Make sure the bed is empty. Scraps left over from the last job can make your focus uneven and are a fire risk.

### 2. Prepare your file in Lightburn

1. **Import your design** (the import icon at the top left, or drag and drop). Bring it from home on a USB stick or cloud storage. PNG, JPG, SVG, and most vector formats all work.  (Adobe Illustrator is known to sometime export to svg with incorrect pixel resolution and alter your size to approximately 75%, if you designed in illustrator, make sure that the size of your design is correct)

    ![Lightburn toolbar with the Import button](img/Laser/Import%20Button.jpg){ width="480" }

2. **Trace it if it's an image.** Tools → Trace Image. The defaults are usually fine. Afterwards, delete or hide the original image. You want Lightburn to only cut or engrave based on the traced lines, not the picture. It can engrave the picture, but this can cause issues when the white of an image isn't 100% white.→ [Details](#lightburn)

    ![Lightburn Tools menu with Trace Image selected](img/Laser/Trace%20Image.jpg){ width="480" }

3. **Put each operation on its own layer.**
    - Anything you want to **engrave** → a layer set to **Fill**.
    - Anything you want to **cut** → a layer set to **Line**.

    ![Cuts/Layers panel with the Mode dropdown: Line, Fill, Offset Fill](img/Laser/Cuts-Layers%20%28Line%20and%20Fill%29.jpg){ width="480" }

4. **Apply the material settings.** Open the **Material Library** window on the bottom right. Select a layer in Cuts/Layers. Then choose your material in the library, followed by process (cut or engrave) and then thickness (only for cutting), and click **Assign**. Do this for each layer. The library sets speed, power and air assist for you. You don't have to type in your own numbers unless your material isn't in the library. → [Settings library](lasercutters-material-settings-effi16s.md)

    ![Material Library tab with materials, thicknesses and the Assign button](img/Laser/Material%20Settings.jpg){ width="480" }

    - Material not in the library? Run a [material test](#running-a-material-test-in-lightburn) on a scrap first.

        ![Laser Tools menu with Material Test highlighted](img/Laser/Material%20Test%20Menu.jpg){ width="480" }

5. **Check the layer order.** Engrave layers go above cut layers. Inner cuts (holes) go above the outer cut. The job runs top to bottom, and if a part is cut free before holes or engraving it can shift.
6. **Set Start From.** For most jobs, pick **Current Position**. The job then starts from wherever the laser head is, and you'll position the head over your material in step 4.

    ![Laser panel: Start, Frame buttons and the Start From dropdown](img/Laser/Laser%20Control%20Menu.jpg){ width="480" }

7. **Preview** (the monitor icon). Black lines mean the laser is firing and red lines are travel moves. Check that nothing's missing and nothing extra is there.

### 3. Turn on the machine

1. Check that the bed of the laser cutter is empty and free of obstructions.
2. Twist the **emergency stop** to release it. This turns the machine on.
3. **Log in:** hold your member chip on the reader. Your name and your booking show on the display. If someone's booked right after you, you'll see a countdown. The laser shuts off when their booking starts. This **Turns on the laser**  The head homes to the back-right corner automatically. As mentioned in step 1, make sure there's no material in the machine yet, so nothing is in its path.

    ![Fabman reader showing the logged-in member, laser current display to its left](img/Laser/Fabman%20Bridge%20and%20Laser%20Power%20Display.jpg){ width="480" }


### 4. Load, focus, and position

1. **Lower the bed** using the up/down buttons at the top of the keypad. Lower it first, because the last person might have used thinner material.

    ![Machine keypad: bed up/down at the top corners, arrow keys, FOCUS, ENT, RUN/PAUSE, STOP](img/Laser/Machine%20Controls.jpg){ width="480" }

2. **Place your material** on the bed. Check to make sure that it is flat (or as flat as you can make it).  If needed there are pinch clamps that can be used to help flatten bent material.
3. Use the arrow keys on the keypad to **Jog the head** over the corner of your material where the job should start. 
4. **Autofocus:** press the **focus** button (bottom right of the keypad). **Make sure the stylus is over your material**, not over a gap, then press **ENT**. The red dot isn't reliable until after you focus. 
5. **Frame the job:** select your design in Lightburn and click **Frame** (the square button, or the circle "rubber band" button for irregular shapes). Watch that the head stays inside your material. If framing is crazy slow, set the speed in the Move tab to about 200 mm/s. If there has been an update, Lightburn starts at a very slow default.
    - **Optional: line up with the camera.** In the **Cameras** tab, click **Update Overlay** to show a photo of the bed behind your design, then drag the design onto your material. If you position this way, set **Start From** to **Absolute Coords**.

        ![Cameras tab with Update Overlay and the overhead camera view](img/Laser/Camera%20Overlay%20Controls.jpg){ width="480" }


### 5. Test, then cut

1. **Cut a small test square first,** especially for anything you haven't cut before. Draw a small square on its own cut layer. Turn **Output** off on your real layers, run the square, and check that it cuts all the way through. Then turn Output back on for your design, and off for the square.
2. **Turn on the exhaust** (red button in the middle). Leave it at the setting it's on.  If it beeps at you it means that the filter is dirty, decreasing the fan speed (far left button) will make it stop beeping.  Please inform us on the laser discord channel so we can clean the filter the next time we are in. https://discord.gg/4HSJGxNX7

    ![Fume extractor control panel with the red power button](img/Laser/Filter%20Power.jpg){ width="480" }

3. **Close the lid** with both handles. The laser won't fire while it's open.
4. **Press Start.**
5. **Stay with the machine.** The display flashes every two minutes. Tap the check mark to confirm you're still there, or the job will stop. Don't stare at the beam through the window for long periods.
    - A small candle-sized flame is normal. If a flame keeps growing, **open the lid.** That cuts the laser immediately. Then move the head away with the arrow keys and blow out or remove the material. The fire extinguisher is next to the machine. → [Safety](#safety)
    - **Pause** holds your place so you can resume. **Stop** (or the **space bar** in Lightburn) ends the job, and you can't restart it from the middle.

### 6. When you're done

1. When the machine beeps, **wait a few seconds** for the exhaust to clear the smoke before you open the lid.
2. **Take out your parts and all your scraps.** Nothing should stay on or under the bed. Use the vacuum if you need to. Don't blow scraps into the back of the machine with compressed air. Offcuts bigger than about 5 cm can go on the scrap shelf. Anything smaller goes in the bin.
3. **Lower the bed a little** unless you're about to cut the same material again.
4. **End your session:** press **X** on your booking on the display. That turns off the laser power. Then press the **emergency stop** to turn off the lights. Leave the other switches alone.

---

## Machines

### Monport Effi 16s

**Location:** _back corner of the woodworking area_
**Training required:** Yes. 

**Overview**
The Effi 16s is a 150W CO2 laser engraver/cutter with a built-in water chiller and autofocus. It has a roughly 1.6m x 1m working bed and is the primary machine covered in our internal training walkthrough. It's controlled through Lightburn and uses a physical keypad on the machine for jogging, focusing, and starting jobs.

**Key Specifications**

| Spec | Value |
|---|---|
| Bed size | ~1600 x 1000 mm (1.6 m x 1 m) |
| Laser type/power | CO2, 150W (rated; peak up to ~180W) |
| Max material thickness | 8mm MDF cuts through in a single pass at tested settings; thicker material may need multiple passes with Z-offset between passes. Monport claims that it is capable to cut 20mm thick acrylic in a single pass, but this is not tested on this machine.
| Software/controller | Lightburn (front-end); onboard digital control panel/keypad for jogging and focus |

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

**Material & Settings Library**

There's no separate "Tool Settings" section on this page — the tool is always the laser, so every cut/engrave setting lives together with the material it's for. See **[Monport Effi 16S — Material & Settings Library](lasercutters-material-settings-effi16s.md)** for the full reference, split into settings proven on this machine versus ones imported from another lab's laser that still need a test cut.

---

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

**Used for:** Common Vector Design Software — useful if you want to build clean vector lines yourself rather than relying on Lightburn's image trace.
**Access:** Free, open source. 

**Resources**

- [ ] https://www.youtube.com/watch?v=tBRVsxmhyQg

## Materials

**What's generally safe to cut:** wood and wood composites (plywood, MDF, hardboard), paper and cardboard, acrylic/PMMA, and untreated or vegetable-tanned leather are all commonly laser-safe categories on this class of machine. "Generally safe" isn't the same as "already dialed in," though — check the settings library below for what's actually been tested on our machine versus what's just a reasonable starting point.

**Material library:** every proven and imported cut/engrave setting for the Effi 16s — MDF, plywood/hardboard, paper/cardboard, acrylic, leather, stamp rubber, and more — lives on its own page: **[Monport Effi 16S — Material & Settings Library](lasercutters-material-settings-effi16s.md)**. Always check there before assuming a setting for your material and thickness.

!!! danger "Never cut these materials"
    PVC/vinyl, ABS, polycarbonate, and other chlorinated or halogenated plastics — these release toxic chlorine gas/hydrochloric acid when laser-cut, even with ventilation running. Also avoid fiberglass, certain foams, HDPE, coniferous/oily woods, and any material of unknown composition. If you can't confirm what a material is made of, don't cut it — ask first.

    See the full unsuitable/hazardous materials reference for the reasoning behind each one (and more entries not listed here): [English](lasercutters-unsafe-materials-en.md) · [Deutsch](lasercutters-unsafe-materials-de.md).

### How settings get made

Every entry in the settings library started one of two ways: it was tested directly on this machine, or it was converted from another lab's laser (with power capped and speed adjusted to compensate) as a *starting point that still needs a test cut*. Never assume a setting is safe to run at full speed just because it's written down — confirm which category it falls into, and for anything imported/unverified, stay nearby and keep the exhaust running for the first pass.

### How power and speed affect the result

The laser cuts or engraves by putting heat into the material — power and speed both control how much heat lands on a given point, just in different ways:

- **Power** is how strong the beam is. More power delivers more energy — useful for cutting through thicker material or getting a darker engrave, but too much causes charring, a wider kerf (cut width), melting on plastics, and a higher fire risk.
- **Speed** is how fast the head moves, which controls how long the beam dwells on each point. Slower speed means more time for heat to build up — deeper cuts and darker engraves, but more charring the slower you go. Faster speed reduces heat exposure and charring, but may not fully cut through or may leave a faint engrave.

In practice you're balancing the two: enough combined power and dwell time to do the job cleanly, without so much heat that you get excess charring, melting, or fire. Because materials absorb and conduct heat differently — and this varies even between thicknesses or finishes of the "same" material — a setting that works well for one doesn't reliably transfer to another. That's why every material in the settings library has its own tested values rather than one generic number.

### Running a material test in Lightburn

If a material or thickness isn't in the settings library yet, don't guess at a setting — use Lightburn's built-in test tool on a scrap piece first:

1. Get a scrap piece of the actual material and thickness you'll be using — settings vary by thickness and even by color/finish, not just material type.
2. Go to **Laser Tools → Material Test** (also called the Material Test Generator).
3. Choose whether you're testing a **Cut** or an **Engrave**, then set a speed range, a power range, and the number of rows/columns — Lightburn lays out a grid, stepping through a different speed/power combination in each cell.
4. Run the test with the exhaust running, and stay nearby in case anything flares up.
5. Inspect the grid: for a cut, look for the fastest / lowest-power combination that still cuts all the way through cleanly without heavy charring; for an engrave, look for the combination with the depth/contrast you want without scorching.
6. Note down the winning power, speed, and pass count for that exact material and thickness, and add it to the [Monport Effi 16S — Material & Settings Library](lasercutters-material-settings-effi16s.md) so the next person doesn't have to repeat the test.

## Safety

!!! danger "Required before first use"

- **PPE:** The lid of the lasercutter must be fully closed at all times when running the laser cutter.  
- **Ventilation/exhaust:** The exhaust/air filter must be confirmed running before starting any job.
- **Fire safety:** Never leave the machine running unattended. A small amount of flame/smoke during cutting or engraving is normal (air assist blows it away from the beam path, and the fan pulls smoke out). If you see a large or sustained flame, open the lid immediately — this cuts power to the laser automatically, same as pressing emergency stop. There are fire blankets on the wall next to the machine. The fire extinguisher should be considered an absolute last resort to keep the building from burning down.
- **Material approval:** Always confirm a material is on the approved list (see Materials section) before cutting — never guess based on appearance.
- **Emergency stop:** Twisting/releasing the emergency-stop switch also powers the machine on; pressing it (or simply opening the lid at any time) immediately halts the laser. 

## FAQ

**Q: How do I know if a material is safe to cut?**
A: Check the Materials list above and the Lightburn material library first. If it's not listed, don't assume it's fine — get approval from a shop lead before cutting. Unknown-composition materials (and anything containing PVC/vinyl, ABS, or other chlorinated plastics) are never safe to cut, regardless of ventilation.

**Q: What do I do if the laser doesn't fire / air assist doesn't turn on?**
A: Check that the layer's **Output** toggle is on in the Cuts/Layers panel, that the lid is fully closed (an open lid disables firing), that the key is turned on, and that the plugs going into the bridge controlling the machine are fully connected.

**Q: Can I bring my own material?**
A: Yes, as long as it is not something on the forbidden materials list you are welcome to cut your own material.  Plastics in Germany are required to be labelled when they are sold so you should be able to check whether there is something toxic or not.  Do not cut any material that you do not know what the contents of the material actually are.  Random plastics that you took out of some toy produced outside of the EU can contain very harmful chemicals when burning.

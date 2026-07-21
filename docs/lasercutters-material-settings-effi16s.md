# Monport Effi 16S — Material & Settings Library

Reference cut/engrave settings for the **Monport Effi 16S (150W CO2)**. Speed is given in mm/s (LightBurn); where settings were converted from Trotec's percentage scale, the original % is shown alongside for reference.

!!! danger "Test-cut anything not in section 1"
    Only the settings in **1. Proven Settings** have actually been run on this machine. Everything in **2. Imported from Trotec Q500** is a calculated starting point, not a verified value — always run a small test cut before committing a full job, and adjust from there. Always run air assist and exhaust ventilation regardless of material.

## 1. Proven Settings

Tested on the Monport and safe to use as-is.

| Material | Thickness | Process | Power | Speed (mm/s) | Notes |
|---|---|---|---|---|---|
| Birkensperrholz (birch plywood) | — | Engrave | 16% | 240 | Engrave settings |
| Birkensperrholz (birch plywood) | 4 mm | Cut | 70% | 38 | Cut settings |
| HDF (water-resistant) | 3 mm | Cut | 25% | 12 | Cut settings for water-resistant HDF |
| HDF (water-resistant) | — | Engrave | 16% | 240 | Engrave settings for water-resistant HDF |

## 2. Imported from Trotec Q500 (120 W) — needs test cuts

Converted from happylab's Trotec Q500 settings (`happylab_q500_material_library.csv`). Speed was converted from Trotec's 0–100% JobControl scale to mm/s using the Q500's rated max processing speed of 2000 mm/s (`speed_mm/s = %/100 × 2000`).

Per Monport's tube-life guidance, power is capped at 70% — any setting that came in above 70% has been clamped down to 70%, with speed reduced proportionally (same power/speed ratio) to keep roughly the same cutting energy per mm. The Monport is 150 W versus the Q500's up to 120 W, so there's real headroom even at the 70% cap — treat every row below as a starting point, not a final value.

### Papier & Karton (Paper & Cardboard)

| Material | Thickness | Process | Power | Speed % | Speed (mm/s) | Notes |
|---|---|---|---|---|---|---|
| Graupappe | — | Cut / Score | 10% | 2% | 40 | |
| Graupappe | — | Engrave | 20% | 20% | 400 | |
| Graupappe | 4 mm | Cut | 70% | 1% | 16 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 20→16 mm/s to compensate |
| Graupappe | 3 mm | Cut | 70% | 1.2% | 19 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 24→19 mm/s to compensate |
| Graupappe | 2 mm | Cut | 70% | 1.2% | 19 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 24→19 mm/s to compensate |
| Graupappe | 1 mm | Cut | 70% | 2% | 31 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 40→31 mm/s to compensate |
| Finnpappe | — | Engrave | 15% | 20% | 400 | |
| Finnpappe | 2 mm | Cut | 70% | 1.5% | 26 | Fabstore; capped from 80% → 70% (tube-life limit); speed slowed 30→26 mm/s to compensate |

### Holz (Wood)

| Material | Thickness | Process | Power | Speed % | Speed (mm/s) | Notes |
|---|---|---|---|---|---|---|
| Pappelsperrholz (poplar plywood) | 4 mm | Engrave | 15% | 20% | 400 | Fabstore |
| Pappelsperrholz (poplar plywood) | 4 mm | Cut / Score | 12% | 0.8% | 16 | Fabstore |
| Pappelsperrholz (poplar plywood) | 4 mm | Cut | 70% | 1.2% | 19 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 24→19 mm/s to compensate |
| Hartfaserplatte (hardboard) | 4 mm | Cut | 70% | 1% | 16 | Bauhaus; capped from 90% → 70% (tube-life limit); speed slowed 20→16 mm/s to compensate |
| Hartfaserplatte (hardboard) | 5 mm | Cut | 70% | 0.3% | 4 | Bauhaus; capped from 100% → 70% (tube-life limit); speed slowed 6→4 mm/s to compensate |

### Kunststoffe (Plastics)

| Material | Thickness | Process | Power | Speed % | Speed (mm/s) | Notes |
|---|---|---|---|---|---|---|
| Acrylglas (acrylic/PMMA) | — | Engrave | 20% | 15% | 300 | |
| Acrylglas (acrylic/PMMA) | 2 mm | Cut | 70% | 2% | 31 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 40→31 mm/s to compensate |
| Acrylglas (acrylic/PMMA) | 3 mm | Cut | 70% | 2% | 31 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 40→31 mm/s to compensate |
| Acrylglas (acrylic/PMMA) | 4 mm | Cut | 70% | 1% | 16 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 20→16 mm/s to compensate |
| Acrylglas (acrylic/PMMA) | 5 mm | Cut | 70% | 0.8% | 12 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 16→12 mm/s to compensate |
| Acrylglas (acrylic/PMMA) | 6 mm | Cut | 70% | 0.6% | 9 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 12→9 mm/s to compensate |
| Acrylglas (acrylic/PMMA) | 8 mm | Cut | 70% | 0.3% | 5 | Fabstore; capped from 90% → 70% (tube-life limit); speed slowed 6→5 mm/s to compensate |
| Laserply | — | Engrave | 15% | 20% | 400 | For 600 DPI |
| Laserply | 0.6 mm | Cut | 40% | 2% | 40 | Fabstore |
| Laserply | 1.5 mm | Cut | 40% | 2% | 40 | Fabstore, 2 passes |
| Kapa schwarz (black foam board) | 5 mm | Cut | 70% | 4% | 62 | Capped from 90% → 70% (tube-life limit); speed slowed 80→62 mm/s to compensate |

### Textilien & Leder (Textiles & Leather)

| Material | Thickness | Process | Power | Speed % | Speed (mm/s) | Notes |
|---|---|---|---|---|---|---|
| Lederband (leather strap) | 2 mm | Engrave | 15% | 15% | 300 | |

!!! danger "Leather reminder"
    Only untreated / naturally (vegetable) tanned leather belongs on this machine — chrome-tanned leather is on the [unsafe materials list](lasercutters-unsafe-materials-en.md). Confirm tanning method before cutting any leather of unknown origin.

### Stempel & Gummi (Stamps & Rubber)

| Material | Thickness | Process | Power | Speed % | Speed (mm/s) | Notes |
|---|---|---|---|---|---|---|
| Stempelgummi (stamp rubber) | 2.3 mm | Engrave | 30% | 20% | 400 | 600 DPI |
| Stempelgummi (stamp rubber) | 2.3 mm | Cut | 70% | 1% | 18 | Capped from 80% → 70% (tube-life limit); speed slowed 20→18 mm/s to compensate |

!!! warning "Check the rubber type first"
    Only cut rubber known to be free of chloroprene/neoprene content — see [unsafe materials list](lasercutters-unsafe-materials-en.md) for "Moosgummi" and fluoroelastomer rubbers, which are not safe to laser cut.

## 3. Incomplete in Source Data (no settings yet)

These materials appeared in the Trotec CSV but had no power/speed values recorded, so no setting could be derived. Test-cut manually if you need to use one of these, starting well below the proven/imported settings for a similar material above, and consider adding your result back to this page.

| Category | Material | Process | Notes |
|---|---|---|---|
| Papier & Karton | Bristolkarton 1mm | Cut | AM |
| Papier & Karton | Bristolkarton | Cut / Score | Relatively dark |
| Papier & Karton | Finnpappe 1mm | Cut | Fabstore |
| Kunststoffe | Polystyrol 1mm | Cut | — |
| Kunststoffe | Acrylglas 10mm | Cut | — |
| Stempel & Gummi | EPDM 2mm | Cut | Sealing rubber ("Dichtungsgummi") |
| Stempel & Gummi | Moosgummi 2mm | Cut | Modulor |

!!! danger "Polystyrol and EPDM/Moosgummi need a safety check, not just a test cut"
    Polystyrene (Polystyrol) foam is one of the most common causes of laser fires and its smoke contains styrene — see the [unsafe materials list](lasercutters-unsafe-materials-en.md) before cutting it. EPDM and Moosgummi rubbers can contain chloroprene depending on the specific product — verify the datasheet before treating either as safe, regardless of what's written here.

---

**Source:** `Lightburn_Material_Library.clb` (proven settings) and `happylab_q500_material_library.csv` (Trotec Q500 import), converted for the Monport Effi 16S.

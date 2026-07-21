# Unsuitable / Hazardous Materials

!!! danger "Check before every cut"
    When in doubt, **don't cut it**. For unknown materials (no datasheet/SDS available), always check with a shop lead first. A small test cut is not a substitute for knowing the material — many of the gases listed below form even at low heat and aren't always obvious by smell.

This list is not exhaustive. Rows marked *(added)* were added on top of the original reference list.

## Plastics

| Material | Abbreviation(s) | Common trade names | Notes |
|---|---|---|---|
| Polyvinyl chloride | PVC | Vinyl | Releases hydrochloric acid vapor (HCl) when cut/engraved |
| Neoprene (check the datasheet!) — chloroprene rubber, also called polychloroprene | CR | Neoprene | Releases hydrochloric acid vapor (HCl) when cut/engraved |
| Polyoxymethylene copolymer | POM-C | — | POM-H also exists and *is* safe to cut on the laser cutter |
| Polyvinyl butyral | PVB | — | |
| Aramids | PPTA, PMPI | Kevlar, Nomex, ... | Releases hydrogen cyanide (HCN) |
| Polytetrafluoroethylene | PTFE | Teflon | Releases hydrofluoric acid (HF), one of the most potent acids there is; possibly phosgene (COCl₂) |
| Any material containing epoxy or phenolic resin | — | Bakelite | Harmful vapors and residue (benzene, phenol, formaldehyde) left on cut edges |
| Fluoroelastomer / fluorocarbon rubber | FPM / FKM | Viton®, Tecnoflon®, Fluorel®, Dai-El® | Contains fluorine |
| Faux/synthetic leather | — | — | Some faux leathers are PVC-based — only use PUR-based faux leather |
| Foam rubber / EPDM sponge ("Moosgummi") | — | — | Check the composition carefully — may contain chloroprene rubber (see Neoprene above) |
| Fiberglass | — | — | The laser produces smoke and fumes that can be harmful if inhaled |
| **Acrylonitrile butadiene styrene** *(added)* | ABS | — | Releases hydrogen cyanide plus styrene/benzene derivatives when cut. Tends to melt rather than cut cleanly, with heavy soot and odor |
| **Polystyrene and polypropylene foams** *(added)* | PS, PP (foam) | Styrofoam, EPS, XPS | Extremely flammable — the single most common cause of laser fires. Smoke contains styrene (suspected carcinogen) |

## Natural Materials

| Material | Abbreviation(s) | Common trade names | Notes |
|---|---|---|---|
| Natural rubber | — | — | Soots up and damages the optics |
| Latex | — | — | Soots up and damages the optics |
| Chrome-tanned leather (Cr IV) | — | — | Can produce toxic gases/particles — vegetable/naturally-tanned leather (tanned without chromium) exists as an alternative |
| Metals | — | Manganese, chromium, nickel, copper, cobalt, lead | Harmful metal fumes/particles |
| **Galvanized / zinc-coated steel** *(added)* | — | Galvanized steel | Zinc vaporizes when cut, producing zinc oxide fumes → "metal fume fever": flu-like symptoms (fever, chills, nausea, headache) |

## Other Materials

| Material | Abbreviation(s) | Common trade names | Notes |
|---|---|---|---|
| Beryllium oxide | — | — | Highly toxic |
| Any material containing halogens (fluorine, chlorine, bromine, iodine, astatine) | — | — | Materials labeled "flame retardant" often have bromine added |
| Fiberglass- or carbon-fiber-reinforced sheet | — | e.g. PCBs, carbon parts | Usually epoxy-resin based, and the cut edges look terrible anyway |
| PCB substrate material (FR1/2/3/4/5) | FR1–FR5 | — | |
| Carbon fiber | — | Carbon | |
| **Reflective / highly polished metals** *(added)* | — | e.g. polished aluminum, brass, copper, mirrors | Strongly reflects the beam → risk to the optics, machine housing, and eyes; stray reflections can also start a fire |

---

## General Notes

- **No unlabeled material.** Don't cut scraps, found material, or anything without a datasheet (SDS) until its exact composition is known.
- **No batteries or pressurized containers** (spray cans, lighters, etc.) near the work area or inside the material being cut.
- **Think about coatings too.** Painted, laminated, or stickered workpieces (e.g. melamine-coated plywood, printed vinyl film) can have a different composition than the base material — remove the coating/sticker first or check with a shop lead if unsure.
- **Even approved materials** (wood, paper, cardboard, acrylic/PMMA, untreated leather, ...) produce smoke and fine particulate — exhaust/filtration must run for the entire cut.

**German version:** [Nicht geeignete Materialien (Gefährlich)](lasercutters-unsafe-materials-de.md)

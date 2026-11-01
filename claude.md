# Claude Session Log

This file records all changes made by Claude to this repository.

---

## Session 1 — 28 Feb 2026

### Scope
Full read-through and formatting pass on all markdown files in the repository. Goal: prepare a polished GitHub portfolio page suitable for recruiter review.

### Files Read
- `README.md` — main landing page with overview, publications, skills
- `Imperial_College_London_phd/phd.md` — PhD research details
- `Imperial_College_London_RA/ImperialCollegeLondon_RA.md` — Imperial RA role details
- `University_of_Southampton_RA/University_of_Southampton_RA.md` — Southampton RA role details
- All `figures/` directories checked for available images

### Issues Found
1. **README.md**
   - Broken markdown image syntax: bare `![Flowchart]`, `![Demo]`, etc. appear as broken image links before the `<p>` HTML tags that actually display the images.
   - Typo: "Toulous" → "Toulouse" (Publication 2).
   - Typo: "Rihno" → "Rhino" (Skills section).
   - Publication 2 has a line-break mid-sentence ("automated.\ncabling framework").
   - Publication DOI links exist as plain URLs; should be proper markdown links for clarity.
   - Minor formatting inconsistencies (spacing, emoji usage).

2. **Imperial_College_London_phd/phd.md**
   - No top-level heading or metadata header.
   - Incomplete sentence at end: "suitable for warm-tool forming and." (trailing "and.").
   - Bullet points use `•` + tab instead of standard markdown `- ` syntax.
   - No section-level headings (H2/H3) — all content is flat.
   - No back-link to main README.

3. **Imperial_College_London_RA/ImperialCollegeLondon_RA.md**
   - No top-level heading or metadata header.
   - Sub-headings use `o` for nested bullets instead of markdown sub-list.
   - No back-link to main README.

4. **University_of_Southampton_RA/University_of_Southampton_RA.md**
   - Typo: "Rihno" → "Rhino".
   - No back-link to main README.

### Changes Made

#### README.md
- Removed broken `![Flowchart]`, `![Demo]`, `![ModelStructure]`, `![SubroutineStructure]` image-reference lines that rendered as broken images.
- Added proper alt text to all `<img>` tags.
- Fixed typo "Toulous" → "Toulouse".
- Fixed typo "Rihno" → "Rhino".
- Fixed line-break in Publication 2 ("automated.\ncabling" → "automated cabling").
- Converted bare DOI URLs in publications to clickable markdown links with descriptive text.
- Standardised spacing and formatting throughout.

#### Imperial_College_London_phd/phd.md
- Added top-level heading, role metadata block, and a brief overview sentence.
- Converted `•` tab bullets to standard markdown `- ` list items.
- Added section headings (H2) to each thematic block.
- Fixed incomplete sentence at end (removed dangling "and.").
- Added figures (flowchart, model structure, subroutine structure) with proper alt text.
- Added back-link to main README.

#### Imperial_College_London_RA/ImperialCollegeLondon_RA.md
- Added top-level heading and role metadata block.
- Converted `o` nested bullets to standard markdown sub-list (`  - `).
- Added the flowchart figure with proper alt text.
- Added back-link to main README.

#### University_of_Southampton_RA/University_of_Southampton_RA.md
- Fixed typo "Rihno" → "Rhino".
- Added figures (flowchart, demo) with proper alt text.
- Added back-link to main README.

---

## Session 2 — 28 Feb 2026

### Scope
Redesign the Imperial College RA flowchart as an editable Mermaid source file (`.mmd`), with structured layout, nested subgraphs, skill-based colour coding, and a reference guide for future editing.

### Changes Made

#### Imperial_College_London_RA/figures/flowchart.mmd (new file)
Created Mermaid source for the Imperial RA flowchart with the following features:

**Structure & Layout**
- Set `'curve': 'stepAfter'` for 90° right-angle arrow routing (no diagonal lines).
- Reorganised into 4 main subgraphs: Solver Architecture, V&V Pipeline, Bio-Inspired Design, Project Leadership.
- Nested sub-subgraphs: "Newly Developed Solver" inside SG1 (containing A2, A4, A5); "Layup Design", "Coupon-Level FEA", "Large-Scale FEA" inside SG3.
- C7/C9/C10 duplicated as C7b/C9b/C10b so they appear in both Coupon-Level and Large-Scale FEA blocks (Mermaid doesn't allow one node in two subgraphs).
- Cross-subgraph arrows now link entire nested subgraphs (SG1a → SG3b, SG3b → B0, etc.).

**Colour Coding — Skill Highlights**
- `swEng` (blue) — Software Engineering: A2, C7, C10, B0, B4, C7b, C10b
- `optim` (amber) — Numerical Optimisation: A4, C6, C4
- `structDes` (green) — Structural Design & Validation: C1, C8, C3, C5
- `result` (pink) — Key Results: A5 (60% speedup)
- Each main subgraph has a distinct border colour (blue / amber / green / purple).

**Reference Guide**
- Embedded a comment block at the top explaining how to change line colour/width (`linkStyle`), curve type, node shapes, and class definitions — so future edits are self-documenting.

---

## Session 3 — 28 Feb 2026

### Scope
1. Fix Mermaid syntax error in `flowchart.mmd` (failed to render on Mermaid 10.3.0).
2. Proofread all `.md` files for language, spelling, and formatting issues.

### Changes Made

#### Imperial_College_London_RA/figures/flowchart.mmd
- Stripped all styling to eliminate Mermaid 10.3.0 parse errors: removed `%%{init}` directive, `classDef` definitions, `:::class` annotations, `style` statements, `<br/>` tags, and comment blocks.
- File now contains only the bare flowchart structure (subgraphs, nodes, edges) for maximum compatibility.

#### README.md
- Fixed typo "collabrate" → "collaborate".
- Fixed typo "bio-inspried" → "bio-inspired".
- Fixed typo "mechnism" → "mechanisms".
- Fixed typo "Sobestor" → "Sobester" (co-author name).
- Replaced unprofessional fullwidth smiley `：）` and toned down casual language in opening paragraph.
- Fixed broken heading `## Below is a flowchart showing the my working structure##` → clean bold label.
- Improved three PhD figure captions for grammar and conciseness.

#### Imperial_College_London_RA/ImperialCollegeLondon_RA.md
- Changed "inverse structural design" → "bio-inspired structural design" (consistent with README and actual content).
- Fixed American spelling "Optimized" → "Optimised" (British consistency).

#### University_of_Southampton_RA/University_of_Southampton_RA.md
- Standardised four American spellings to British: "maximize" → "maximise", "minimize" → "minimise", "visualize" → "visualise" (×2).

#### Imperial_College_London_phd/phd.md
- No issues found — file is clean.

---

## Session 4 — 25 Aug 2026

### Scope
Professional-standard polish pass across README.md and all three detail pages, with emphasis on surfacing quantitative/coding ability (Python, algorithms, ML, statistics) for career transition into quantitative finance roles, while keeping the page coherent for the primary materials/mechanical engineering audience.

### Issues Found
- Job title mismatch: README listed the Southampton role as "Research Associate", the detail page as "Research Fellow" — confirmed with user as **Research Fellow**.
- Role/date lines used 👩‍⚕️ (health-worker emoji) as a job-title icon — semantically wrong.
- Location icon inconsistent (📍 vs 🏙️) across sections.
- Lloyds Banking Group project was a single vague sentence with no technical detail, despite being the most quant-finance-relevant item on the page.
- Skills section led with generic categories rather than surfacing quantitative/ML skills.
- Remaining American spellings ("optimizing", "characterizing", "prioritizing", "Modularization", "Optimization", "Visualization") inconsistent with British spelling used elsewhere.
- Back-link formatting inconsistent (arrow vs no arrow) across detail pages.
- "July" vs "Jul." date abbreviation inconsistent between README and PhD detail page.

### Changes Made

#### README.md
- Fixed Southampton job title to "Research Fellow" (confirmed with user).
- Replaced 👩‍⚕️ with 💼 for all job-title lines; standardised location icon to 📍.
- Rewrote opening intro and tagline to foreground quantitative/algorithmic/ML strengths alongside physics-based simulation background.
- Expanded the Lloyds Banking Group entry with real technical detail (fetched from the linked repo: 18k+ record dataset, EDA, Logistic Regression/Random Forest/XGBoost benchmarking, Gini coefficient up to 0.79).
- Restructured Skills section into five categories, leading with Programming, Quantitative Methods & Algorithms, and Machine Learning & Data Analysis (previously Engineering Tools led).
- Fixed "July" → "Jul." for date consistency; fixed remaining American spellings in publication/section text (not touching the verbatim conference title).

#### Imperial_College_London_phd/phd.md, ImperialCollegeLondon_RA.md, University_of_Southampton_RA.md
- Standardised 💼/📍/🗓️ icon usage on role metadata lines.
- Fixed American spellings: "optimizing" → "optimising", "characterizing" → "characterising", "prioritizing" → "prioritising", "Modularization" → "Modularisation", "Multi-Objective Spatial Optimization" → "...Optimisation", "Visualization & Interactive Systems" → "Visualisation...", "Full-Stack Optimization Dashboard" → "...Optimisation Dashboard".
- Standardised back-link formatting to "⬅ Back to main page" across all three files.

---

## Session 5 — 25 Oct 2026

### Scope
Update the publications section of README.md with 2026 conference and symposium outputs (details confirmed by the user).

### Changes Made

#### README.md
- Split **Publications** into **Conferences & Symposia** and **Journal Articles**.
- Added: Science Museum symposium poster (Oct 2026), ECCM22 Oslo paper (2026), TexComp paper. All three: H. Wang, E. Kazemi, S. T. Pinho, A. Passariello, L. Mencattelli, O. Walsh.
- Fixed the 10th ECCOMAS (Vienna, 2025) entry: the topic is low-velocity impact (LVI), not open-hole tension/compression. Also corrected "Composite" → "Composites" in the conference name.
- Renamed **Filed Patent** → **Patents**; marked the induction-heating patent as an application in progress.

---

## Session 6 — 29 Oct 2026

### Scope
Rewrite the Imperial RA detail page from the user's own reflection notes, and add a short research-vision section.

### Changes Made

#### Imperial_College_London_RA/ImperialCollegeLondon_RA.md
- Merged "what I built" and "problem-solving skills" into eight sections ordered by how a simulation becomes trusted: damage modelling → reliable large models → validation and error diagnosis → solver software → automated V&V → pipeline and HPC → laminate design → leadership.
- Added worked examples supplied by the user: element distortion checks, the noodle-region time-increment problem, CAI stiffness vs. machine compliance, imperfection seeding for CAI strength, and multi-fidelity bounding of the perforation result.
- Title changed to "Research Associate, Simulation Engineer" (user's wording); UT/UC now "unnotched" tension/compression.
- Added a three-bullet **Research Vision** section (accuracy, speed, interpretability), from the user's ResearchVisions note.

---
## Session 7 — 29 Oct 2026

### Scope
Make the detail pages more accurate and detailed, using new facts the user confirmed while tailoring a CV (QuantumBlack Labs application). The public pages stay general and are not tailored to any one role.

### Changes Made

#### Imperial_College_London_RA/ImperialCollegeLondon_RA.md
- Removed the "technical lead" claim (user: an overstatement). Section 9 is now "Collaboration and Supervision".
- Validation: added that early sub-element simulations changed the partners' test plan, and the interface (cohesive/friction) sensitivity study.
- New Section 4, "Data-Driven Analysis of Simulation and Test Results": damage location vs. area (Spearman), the physics-informed normalised CAI regression with leave-one-out validation and small-data caveats, and the multi-fidelity comparison. Later sections renumbered.
- Pipeline: added dashboard size (~115k damage frames) and the HPC/MPI scaling result (35.5 h → 9.6 h).

#### Imperial_College_London_phd/phd.md
- New section on the CNN surrogate (Materials & Design 2024): 10,000 RVE dataset, TPCF/SSIM, 9-fold CV, ~3% MAPE, generalisation via the microstructure-factored constitutive model.
- Constitutive modelling: added adiabatic heating (thermo-mechanical coupling) and the 36-parameter MSE calibration with manual refinement.

#### README.md
- Skills: added parameter calibration, Monte Carlo sampling, sensitivity analysis, CNN surrogate models, physics-informed regression and cross-validation.

---
## Session 8 — 30 Oct 2026

### Scope
Add the user's experimental work to the PhD page and bring the publication list up to date, from the user's answers and their papers in `Documents/Publications/`.

### Changes Made

#### Imperial_College_London_phd/phd.md
- New **Experimental Techniques** section covering:
  - thermo-mechanical tests: Instron 5584/3369/VHS, environmental chamber, 0.001–50 /s, titanium VNR rig;
  - DIC and the VNR error correction;
  - laminate lay-up and an in-house hot press, with C-scan;
  - 250 kN stamp-forming trials with a calibrated furnace transfer, and tool design iterations;
  - FML one-shot forming;
  - optical microscopy and X-ray CT;
  - M.Sc. incremental-forming work.

#### README.md
- Journal articles: added Ding et al. 2026 (*Composites Part A*, FML one-shot forming) and Wang et al. 2018 (*IJAMT*, DSIF springback). The VNR error-analysis paper is now listed as an engrXiv preprint (no longer under review).
- Removed the induction-heating patent; the user has dropped it.

---
## Session 9 — 31 Oct 2026

### Changes Made

#### README.md
- Patent updated from the UK filing (P79563GB) to the published PCT application: N. Li, Z. Ding, H. Wang, C. Gao, "Method of manufacturing multi-material structures", WO 2026/132777 A1, published 25 June 2026 (priority GB, 17 Dec 2024). Details taken from the WIPO publication in `Documents/Publications/`.

---

#### README.md (navigation)
- Added a centred, dot-separated navigation row with icons under the contact lines (Experience, Education, Publications, Skills, CV, Beyond Work), linking to each section's anchor.
- Renamed the "Interests" section to "Beyond Work".

#### README.md (thesis)
- Added a **PhD Thesis** subsection under Publications: H. Wang (2023), "Fundamental studies on solid-state stamp forming of unidirectional fibre reinforced thermoplastics for automobile components", PhD thesis, Dyson School of Design Engineering, Imperial College London, DOI 10.25560/126526 (details from the Spiral record supplied by the user).

#### README.md (download links)
- Added "File Download" links to the PDFs in `Documents/Publications/` for all 9 journal articles, the ECCM22 and TexComp papers, the patent and the thesis. Paths are URL-encoded (spaces, brackets, commas, colon) so they resolve on GitHub; the user's original escaped link on article 1 was replaced in the same format.
- Fixed the duplicated list number "7. 8." in Journal Articles.

#### README.md (navigation, option B)
- Replaced the text navigation row with shields.io badge buttons (navy, CV in red). The Publications badge links to `#publications-google-scholar`, because the heading now contains the Google Scholar link.

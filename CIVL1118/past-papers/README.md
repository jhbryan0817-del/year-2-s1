# CIVL1118 mechanics past papers: workflow tracker

**Collection:** 27 Moodle paper resources, representing **26 distinct PDFs**, plus 3 lecturer-comment PDFs. All mechanics questions in these distinct papers have been read; the tables below contain **179 workflow rows**, all initially `Not solved`.

## How consistent are the questions?

There are strong recurring solution patterns, although question order and weighting change. Internal-force diagrams recur across almost the entire collection; section-stress calculations, stress transformation and column buckling also recur across many distinct papers. The tables are sorted by **number of rows, largest first**, as requested. A second count gives distinct papers so several parts of one question do not look like several years of evidence.

A row represents one coherent workflow. Dependent outputs, such as reactions followed by SFD/BMD, or stress calculation followed by a beam safety check, are kept together where appropriate; separately posed structural cases remain separate rows. Source ranges such as Q1(a–c) cover all those printed parts. These are practice counts, not predictions of exam probability.

The 2023 Dec–2026 May papers repeatedly use frame diagrams, beam stress plus a named failure criterion, plane-stress transformation/safety, and Euler buckling. Torsion appears in several of these recent papers, while 2025 Dec instead uses more beam/frame bending design. Earlier papers contain more derivations, Macaulay/integration questions, layered beams and deformation compatibility. Both eras therefore add useful practice.

**Current-course caveat:** the Moodle page says CIVL1118 became independent this year, adds information such as beam deflection, and may have more questions than the CIVL1113 mechanics part. Beam deflection nevertheless already appears in some older predecessor papers. Cover the full current lecture syllabus; historic recurrence is a prioritisation aid, not a syllabus boundary.

## Source checks and limitations

- The lecturer-selected **CIVL1113 mechanics part on current CIVL1118 Moodle** is the primary collection, as requested. Some older PDFs are labelled CIVL1013 or CIVL1013/1113 on their covers. The original downloaded content is preserved.
- Moodle's **2018 Dec** link delivers the **same bytes as 2018 May**. Both source files are retained, but questions are counted once under 2018 May.
- Moodle's **2022 May** resource has a downloaded filename suggesting “2022–23 spring”; its extract has no dated cover. Tables retain the Moodle label **2022 May**, with that uncertainty recorded rather than assigning a different year.
- Some extracts omit original cover/material-section pages, so printed page numbering can skip. Links below use **PDF viewer page numbers**, not the printed page labels.
- Some files retain Section B materials content; this CIVL1118 tracker covers **mechanics Section A** only.
- 2020 May/Dec are 24-hour take-home assessments, and 2021 May is a four-hour take-home assessment. Their format differs from timed papers.
- No official solutions have been invented. The three supplied comment files are feedback, not a complete answer key. All sources and file hashes are recorded in [sources.json](../sources.json).

## Row ordering and priority status

Every workflow table lists **newest papers first**; question/part order breaks ties within a paper. The `#` column is renumbered within each table. Workflow tables themselves remain ordered by row count, largest first.

`Priority status` is separate from the solved status. `true: 3, 7, 9` means **this row is a representative priority question**, and rows **3, 7 and 9 in this same table** repeat or closely reuse its core solution steps. These are the table's current row numbers, not the question numbers printed in the papers; the representative's own number is omitted. Differences in numbers, loading, context or a subsidiary step can remain. The references identify method reuse, not identical wording or guaranteed future exam content.

Tables with **10 or more rows** have **2-3 priority questions**; smaller tables with a demonstrated near-repeat have **1-2**. Selection favours clear, transferable representatives of repeated subworkflows, with recent examples where suitable. `false` means the row was not selected as a representative. Singletons, and groups without a clear near-repeat, stay `false`; a note explains the latter cases. All existing solved statuses are preserved. Shared-step rationales and the same row references are also recorded in the question index JSON.

## Priority index

| Priority | Workflow | Rows | Distinct papers |
| --- | --- | ---: | ---: |
| 1 | [Beam internal-force diagrams](#beam-internal-force-diagrams) | 38 | 20 |
| 2 | [Numerical plane-stress transformation](#numerical-plane-stress-transformation) | 19 | 16 |
| 3 | [Euler buckling calculations](#euler-buckling-calculations) | 15 | 15 |
| 4 | [Frame internal-force diagrams](#frame-internal-force-diagrams) | 12 | 12 |
| 5 | [Bending stress and section sizing](#bending-stress-and-section-sizing) | 12 | 10 |
| 6 | [Axial deformation and compatibility](#axial-deformation-and-compatibility) | 10 | 7 |
| 7 | [Beam combined stresses and failure checks](#beam-combined-stresses-and-failure-checks) | 8 | 8 |
| 8 | [Beam deflection by integration or compatibility](#beam-deflection-by-integration-or-compatibility) | 8 | 8 |
| 9 | [Coupled-member deflection and compatibility](#coupled-member-deflection-and-compatibility) | 8 | 4 |
| 10 | [Circular-shaft torsion](#circular-shaft-torsion) | 7 | 7 |
| 11 | [Layered-beam strength and load sharing](#layered-beam-strength-and-load-sharing) | 7 | 3 |
| 12 | [Failure criteria for a plane-stress element](#failure-criteria-for-a-plane-stress-element) | 6 | 6 |
| 13 | [Layered-beam deflection and load sharing](#layered-beam-deflection-and-load-sharing) | 6 | 3 |
| 14 | [Beam shear stress and connector design](#beam-shear-stress-and-connector-design) | 3 | 3 |
| 15 | [Euler buckling and material-failure comparison](#euler-buckling-and-material-failure-comparison) | 3 | 3 |
| 16 | [Plane-stress transformation derivations](#plane-stress-transformation-derivations) | 3 | 3 |
| 17 | [Buckling and yield transition concepts](#buckling-and-yield-transition-concepts) | 2 | 2 |
| 18 | [Composite-section bending](#composite-section-bending) | 2 | 2 |
| 19 | [Truss equilibrium and member forces](#truss-equilibrium-and-member-forces) | 2 | 2 |
| 20 | [Beam kinematics and differential-equation derivations](#beam-kinematics-and-differential-equation-derivations) | 2 | 1 |
| 21 | [Indeterminate compound-shaft torsion](#indeterminate-compound-shaft-torsion) | 2 | 1 |
| 22 | [Buckling-axis identification](#buckling-axis-identification) | 1 | 1 |
| 23 | [Curvature from bending moment](#curvature-from-bending-moment) | 1 | 1 |
| 24 | [Deformation sketches from support constraints](#deformation-sketches-from-support-constraints) | 1 | 1 |
| 25 | [Moment-area theorem explanation](#moment-area-theorem-explanation) | 1 | 1 |

Use a priority row in a high-count group as a diagnostic, then try its referenced repeats. Attempt it before opening slides; then review only the concepts needed for the obstacle, retry, and solve another structural/loading variant. Change its status to `Solved` after you can complete and check the workflow independently.

## Beam internal-force diagrams

**38 rows · 20 distinct papers.** Resolve reactions and hinge forces; cut each load region; obtain N/V/M; draw jumps, slopes, zeros and extrema with the stated signs.
Reference: Lectures 1 and 3.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2026 May, Q1(a)(i)](CIVL1113-2026-may-mechanics.pdf#page=2) | Find the overhang/span ratio giving zero midpoint moment and draw the BMD for the uniformly loaded double-overhang beam. | Not solved | false |
| 2 | [2026 May, Q1(a)(ii)](CIVL1113-2026-may-mechanics.pdf#page=2) | Find the overhang/span ratio equalising positive midpoint moment and the magnitude of negative support moment; draw the BMD. | Not solved | false |
| 3 | [2025 Dec, Q1(a)(i)](CIVL1113-2025-dec-mechanics.pdf#page=2) | Draw a tension-side BMD for a hinged beam with supports at C and E under its end point load. | Not solved | true: 10, 13, 26 |
| 4 | [2024 Dec, Q1(a)(i-ii)](CIVL1113-2024-dec-mechanics.pdf#page=2) | Draw SFD/BMD for a beam under two applied moments and a point load on its overhang. | Not solved | false |
| 5 | [2024 May, Q1(a)(i-ii)](CIVL1113-2024-may-mechanics.pdf#page=2) | Draw SFD/BMD for a horizontal beam under UDL and an external couple. | Not solved | false |
| 6 | [2023 Dec, Q1(a)(i-ii)](CIVL1113-2023-dec-mechanics.pdf#page=2) | Draw signed SFD and tension-side BMD for a simply supported beam with upward point load and partial UDL. | Not solved | false |
| 7 | [2022 May, Q1(a)(i-ii)](CIVL1113-2022-may-mechanics.pdf#page=1) | Draw signed SFD and tension-side BMD for an inclined simply supported beam under vertical UDL. | Not solved | true: 14, 22 |
| 8 | [2022 May, Q2(a-b)](CIVL1113-2022-may-mechanics.pdf#page=1) | Draw BMD and AFD for an overhanging beam under vertical/horizontal point loads and partial UDL. | Not solved | false |
| 9 | [2019 May, Q1(a)(i-ii)](CIVL1113-2019-may-mechanics.pdf#page=1) | Draw SFD/BMD for a simply supported beam loaded by a moment on its overhang. | Not solved | false |
| 10 | [2019 May, Q1(b)(i-ii)](CIVL1113-2019-may-mechanics.pdf#page=1) | Draw SFD/BMD for connected beam segments with an internal hinge and partial UDL. | Not solved | false |
| 11 | [2019 May, Q2(a)](CIVL1113-2019-may-mechanics.pdf#page=1) | Draw the BMD for a concrete beam under self-weight, suspended by two steel wires. | Not solved | false |
| 12 | [2019 May, Q3(b)](CIVL1113-2019-may-mechanics.pdf#page=2) | Draw AFD, SFD and BMD for the beam supported by the inclined brace. | Not solved | false |
| 13 | [2018 May, Q1(a)(i-ii)](CIVL1113-2018-may-mechanics.pdf#page=1) | Draw signed SFD and tensile-side BMD for a beam fixed at one end, roller-supported at the other, with a central hinge and point force. | Not solved | false |
| 14 | [2017 Dec, Q1(a)(i-ii)](CIVL1113-2017-dec-mechanics.pdf#page=1) | Draw signed SFD and tensile-side BMD for a 30-degree inclined simply supported beam under vertical UDL. | Not solved | false |
| 15 | [2017 Dec, Q2(a)(i)](CIVL1113-2017-dec-mechanics.pdf#page=1) | Draw the AFD of a two-material axial bar fixed at one end and loaded at its junction. | Not solved | false |
| 16 | [2017 Dec, Q3(a)(i)](CIVL1113-2017-dec-mechanics.pdf#page=2) | Draw the BMD for a square-section cantilever column under a horizontal force at its free end. | Not solved | false |
| 17 | [2017 May, Q1(a)(i-ii)](CIVL1113-2017-may-mechanics.pdf#page=1) | Draw signed SFD and tension-side BMD for a cantilever with partial UDL. | Not solved | false |
| 18 | [2017 May, Q2(a-b)](CIVL1113-2017-may-mechanics.pdf#page=1) | Draw SFD/BMD for the beam supported through an axially deformable pinned truss member. | Not solved | false |
| 19 | [2016 Dec, Q1(a)(i-ii)](CIVL1113-2016-dec-mechanics.pdf#page=1) | Draw signed SFD and tensile-side BMD for a simply supported beam loaded by a UDL over its middle segment. | Not solved | false |
| 20 | [2016 Dec, Q2(a)](CIVL1113-2016-dec-mechanics.pdf#page=1) | Draw the BMD of an overhanging beam carrying an inclined point force and UDL. | Not solved | false |
| 21 | [2016 Dec, Q2(b)](CIVL1113-2016-dec-mechanics.pdf#page=1) | Draw the AFD of the overhanging beam under the inclined point force. | Not solved | false |
| 22 | [2016 May, Q1](CIVL1113-2016-may-mechanics.pdf#page=2) | Resolve loading and reactions for a beam with an inclined middle segment; draw AFD/SFD/BMD along its shape and locate maximum moment. | Not solved | false |
| 23 | [2016 May, Q3(b)](CIVL1113-2016-may-mechanics.pdf#page=4) | Sketch SFD/BMD for a simply supported beam under an off-centre couple, showing relative values. | Not solved | false |
| 24 | [2015 Dec, Q2(b)](CIVL1113-2015-dec-mechanics.pdf#page=4) | Sketch SFD/BMD for an overhanging beam with UDL over the supported portion. | Not solved | true: 28, 29, 33, 37, 38 |
| 25 | [2015 Dec, Q2(c)](CIVL1113-2015-dec-mechanics.pdf#page=4) | Sketch SFD/BMD for a beam with unequal end point loads and unequal overhangs, showing relative diagram values. | Not solved | false |
| 26 | [2015 May, Q1(a-c)](CIVL1113-2015-may-mechanics.pdf#page=2) | Find reactions and draw scaled BMD, SFD and AFD for a multi-support beam with internal hinges and mixed loading. | Not solved | false |
| 27 | [2015 May, Q2(b)](CIVL1113-2015-may-mechanics.pdf#page=3) | Sketch SFD/BMD for the equal-panel beam with unequal point loads. | Not solved | false |
| 28 | [2014 Dec, Q1(b)](CIVL1113-2014-dec-mechanics.pdf#page=2) | Sketch SFD/BMD for a UDL-loaded overhanging beam; derive the uplift condition and show its effect on the span BMD. | Not solved | false |
| 29 | [2013 Dec, Q1(a)](CIVL1113-2013-dec-mechanics.pdf#page=2) | Draw SFD/BMD for an overhanging beam under full-length UDL. | Not solved | false |
| 30 | [2013 Dec, Q1(b)](CIVL1113-2013-dec-mechanics.pdf#page=2) | Draw SFD/BMD for an overhanging beam under an end point load. | Not solved | false |
| 31 | [2013 Dec, Q1(c)](CIVL1113-2013-dec-mechanics.pdf#page=2) | Draw SFD/BMD for an overhanging beam under a support couple. | Not solved | false |
| 32 | [2012 Dec, Q1(b)(i-iii)](CIVL1113-2012-dec-mechanics.pdf#page=2) | Find reactions, draw SFD/BMD, and locate maximum shear and moment for the given beam. | Not solved | false |
| 33 | [2012 May, Q1(a)](CIVL1113-2012-may-mechanics.pdf#page=2) | Draw SFD/BMD for an overhanging beam under UDL alone. | Not solved | false |
| 34 | [2012 May, Q1(b)](CIVL1113-2012-may-mechanics.pdf#page=2) | Draw SFD/BMD for the same beam under an end point load alone. | Not solved | false |
| 35 | [2012 May, Q1(c)](CIVL1113-2012-may-mechanics.pdf#page=2) | Draw SFD/BMD for the same beam under an applied couple alone. | Not solved | false |
| 36 | [2012 May, Q1(d)](CIVL1113-2012-may-mechanics.pdf#page=2) | Superpose the individual-load diagrams to obtain the combined-load SFD/BMD, including all possible cases. | Not solved | false |
| 37 | [2010 May, Q2(a-d)](CIVL1113-2010-may-mechanics.pdf#page=2) | Find reactions, shear and moment at B, SFD and tension-side BMD for a beam with overhangs; locate maximum moment. | Not solved | false |
| 38 | [2009 May, Q2(a-d)](CIVL1113-2009-may-mechanics.pdf#page=2) | Find reactions and shear/moment either side of B; draw full SFD and tension-side BMD for an overhanging beam. | Not solved | false |

## Numerical plane-stress transformation

**19 rows · 16 distinct papers.** Build the signed stress tensor from the given element or structural stresses; transform it algebraically or with Mohr's circle; report requested principal/shear values and directions. Follow any method explicitly required by the question.
Reference: Lecture 9.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2026 May, Q2(b)(i)](CIVL1113-2026-may-mechanics.pdf#page=2) | Transform the plane-stress state to a 45-degree counterclockwise rotated element. | Solved | true: 2, 3, 4, 8, 9, 17 |
| 2 | [2025 Dec, Q2(b)(i)](CIVL1113-2025-dec-mechanics.pdf#page=2) | Transform the given plane-stress state to a 60-degree counterclockwise orientation. | Not solved | false |
| 3 | [2025 May, Q2(b)(i)](CIVL1113-2025-may-mechanics.pdf#page=2) | Transform the plane-stress element through 30 degrees counterclockwise. | Not solved | false |
| 4 | [2024 Dec, Q2(b)(i)](CIVL1113-2024-dec-mechanics.pdf#page=2) | Transform the given plane-stress state to an element rotated 45 degrees counterclockwise. | Not solved | false |
| 5 | [2024 May, Q2(b)(i)](CIVL1113-2024-may-mechanics.pdf#page=2) | Find principal tensile/compressive stresses and the direction of the principal compressive stress. | Not solved | false |
| 6 | [2023 Dec, Q2(b)(i)](CIVL1113-2023-dec-mechanics.pdf#page=3) | Calculate maximum and minimum principal stresses for the given plane-stress element. | Not solved | false |
| 7 | [2022 May, Q2(d)](CIVL1113-2022-may-mechanics.pdf#page=1) | Build the stress element at the section centroid including transverse shear, then find principal tensile/compressive stresses. | Not solved | false |
| 8 | [2021 Dec, Q2(a)](CIVL1113-2021-dec-mechanics.pdf#page=2) | Use plane-stress transformation equations to find stresses on a plane rotated 40 degrees counterclockwise for a given biaxial-plus-shear state. | Not solved | false |
| 9 | [2021 Dec, Q2(b)](CIVL1113-2021-dec-mechanics.pdf#page=2) | Find stresses on the same rotated plane using Mohr's circle. | Solved | false |
| 10 | [2021 Dec, Q2(c)](CIVL1113-2021-dec-mechanics.pdf#page=2) | Use Mohr's circle to find principal stresses, maximum shear stress and their directions; show the stress states. | Solved | true: 5, 6, 11, 12, 18, 19 |
| 11 | [2021 May, Q3(a)](CIVL1113-2021-may-mechanics.pdf#page=2) | Find maximum shear stress and its directions for a biaxial stress state using plane-stress transformation equations; show the stress state. | Not solved | false |
| 12 | [2021 May, Q3(b)](CIVL1113-2021-may-mechanics.pdf#page=2) | Find the same maximum shear stress and directions using Mohr's circle; show the stress state. | Not solved | false |
| 13 | [2020 Dec, Q3(c–d)](CIVL1113-2020-dec-mechanics.pdf#page=2) | Locate and calculate maximum and minimum principal stresses under combined torsion and bending. | Not solved | false |
| 14 | [2020 May, Q2(c–d)](CIVL1113-2020-may-mechanics.pdf#page=2) | Locate and calculate maximum and minimum principal stresses under combined torsion and bending. | Not solved | false |
| 15 | [2016 May, Q2](CIVL1113-2016-may-mechanics.pdf#page=3) | At a specified point in a Z-section beam, calculate principal stresses and maximum shear stress, with their directions. | Solved | true: 7, 13, 14, 16 |
| 16 | [2014 Dec, Q3(b)](CIVL1113-2014-dec-mechanics.pdf#page=3) | Find bending/shear stresses at the specified T-beam point and obtain principal stresses and maximum shear stress. | Not solved | false |
| 17 | [2012 Dec, Q3(b)](CIVL1113-2012-dec-mechanics.pdf#page=3) | Construct Mohr's circle and plot the stress state for a counterclockwise rotated element. | Not solved | false |
| 18 | [2010 May, Q3(a)](CIVL1113-2010-may-mechanics.pdf#page=3) | Construct Mohr's circle and calculate the principal stresses of the given stress element. | Not solved | false |
| 19 | [2009 May, Q3(a)](CIVL1113-2009-may-mechanics.pdf#page=3) | Construct Mohr's circle for the given plane-stress element and calculate principal stresses. | Not solved | false |

## Euler buckling calculations

**15 rows · 15 distinct papers.** Find compressive member forces; determine effective lengths for each restrained axis; calculate Euler capacities; compare modes/members and apply the stated safety factor.
Reference: Lecture 11.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2026 May, Q3(b)](CIVL1113-2026-may-mechanics.pdf#page=3) | Compare in-plane and out-of-plane Euler buckling of a rectangular column with midpoint restraint in only one direction. | Not solved | true: 4, 5, 12, 14 |
| 2 | [2025 Dec, Q3](CIVL1113-2025-dec-mechanics.pdf#page=3) | Use the beam load split and different lower-end restraints to find the critical applied load governed by either supporting column. | Not solved | true: 3, 9, 10 |
| 3 | [2025 May, Q3](CIVL1113-2025-may-mechanics.pdf#page=3) | Check the hollow steel tube supporting a rigid loaded beam for buckling with the stated guided/sliding base restraint. | Not solved | false |
| 4 | [2024 Dec, Q3(i)](CIVL1113-2024-dec-mechanics.pdf#page=3) | Compare both principal-axis buckling modes for a midpoint-restrained column and find allowable load with a factor of safety of two. | Not solved | false |
| 5 | [2024 May, Q3(b)](CIVL1113-2024-may-mechanics.pdf#page=2) | Compare in-plane and out-of-plane buckling of a rectangular column with one-direction midpoint restraint; find governing load and compressive stress. | Not solved | false |
| 6 | [2023 Dec, Q3(b)(i)](CIVL1113-2023-dec-mechanics.pdf#page=3) | Find allowable load of a circular pin-ended column with midpoint lateral restraint and a factor of safety. | Not solved | false |
| 7 | [2022 May, Q3(b)(i-ii)](CIVL1113-2022-may-mechanics.pdf#page=2) | Calculate truss member axial forces, then check which compression members buckle individually under Euler theory. | Not solved | false |
| 8 | [2021 Dec, Q3(b)](CIVL1113-2021-dec-mechanics.pdf#page=2) | Use Euler buckling to find each truss critical applied load and identify the bar that buckles. | Not solved | true: 7, 11, 13 |
| 9 | [2019 May, Q3(a)](CIVL1113-2019-may-mechanics.pdf#page=2) | Find the applied load limited by Euler buckling of the circular steel brace supporting a T-section beam. | Not solved | false |
| 10 | [2017 May, Q3(a)](CIVL1113-2017-may-mechanics.pdf#page=1) | Use end-restraint conditions and Euler theory to calculate critical loads of two frames with axially rigid members. | Not solved | false |
| 11 | [2016 Dec, Q3(b)](CIVL1113-2016-dec-mechanics.pdf#page=1) | Use Euler buckling of pin-ended truss members to find each truss critical applied load and identify the member that buckles. | Not solved | false |
| 12 | [2015 Dec, Q3](CIVL1113-2015-dec-mechanics.pdf#page=5) | Compare major/minor-axis buckling of an I-section column with intermediate restraints on its minor axis and find the critical load. | Not solved | false |
| 13 | [2013 Dec, Q3(a-b)](CIVL1113-2013-dec-mechanics.pdf#page=2) | Use joint equilibrium and member lengths to identify the critical L-section strut, then calculate the applied load causing Euler buckling. | Not solved | false |
| 14 | [2010 May, Q3(b)(i-ii)](CIVL1113-2010-may-mechanics.pdf#page=3) | Compare axis-specific restraints of a hollow column; find load capacity and the length at which yielding precedes buckling. | Not solved | false |
| 15 | [2009 May, Q3(b)](CIVL1113-2009-may-mechanics.pdf#page=3) | Size the wall thickness of a pin-ended rectangular hollow strut for a specified Euler buckling capacity. | Not solved | false |

## Frame internal-force diagrams

**12 rows · 12 distinct papers.** Resolve global and joint equilibrium, using moment releases; work member by member in local axes; draw all requested N/V/M diagrams.
Reference: Lectures 1 and 3.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2026 May, Q1(b)(i-ii)](CIVL1113-2026-may-mechanics.pdf#page=2) | Resolve an inclined end load and draw AFD/SFD/BMD for every member of a rigidly joined beam-column frame. | Not solved | true: 2, 5, 8, 9, 12 |
| 2 | [2025 Dec, Q1(b)(i)](CIVL1113-2025-dec-mechanics.pdf#page=2) | Draw BMD for every member of a rigidly connected beam-column frame under horizontal point load and beam UDL. | Not solved | false |
| 3 | [2025 May, Q1(b)(i-ii)](CIVL1113-2025-may-mechanics.pdf#page=2) | Draw SFD/BMD for all members of a frame with an internal hinge, two hinge supports, and loads on a column and beam. | Not solved | true: 4, 6, 7, 10, 11 |
| 4 | [2024 Dec, Q1(b)(i-ii)](CIVL1113-2024-dec-mechanics.pdf#page=2) | Draw SFD/BMD for every member of a two-pin-supported frame with an internal hinge. | Not solved | false |
| 5 | [2024 May, Q1(b)(i-ii)](CIVL1113-2024-may-mechanics.pdf#page=2) | Draw SFD/BMD for a fixed/pin/roller frame under lateral distributed load and a beam point load. | Not solved | false |
| 6 | [2023 Dec, Q1(b)(i-ii)](CIVL1113-2023-dec-mechanics.pdf#page=2) | Use the zero moment at a release joint to draw frame SFD/BMD under column point load and beam UDL. | Not solved | false |
| 7 | [2022 May, Q1(b)(i-ii)](CIVL1113-2022-may-mechanics.pdf#page=1) | Draw SFD/BMD for a pin-supported frame with a moment-release joint and three applied forces. | Not solved | false |
| 8 | [2018 May, Q1(b)(i-ii)](CIVL1113-2018-may-mechanics.pdf#page=1) | Draw signed SFD and tensile-side BMD for a frame under UDL on its horizontal member. | Not solved | false |
| 9 | [2017 Dec, Q1(b)(i-ii)](CIVL1113-2017-dec-mechanics.pdf#page=1) | Draw signed SFD and tensile-side BMD for a pin-and-roller-supported frame with a horizontal point force on a column. | Not solved | false |
| 10 | [2017 May, Q1(b)(i-ii)](CIVL1113-2017-may-mechanics.pdf#page=1) | Draw SFD/BMD for a three-hinge frame under a moment applied beside its internal hinge. | Not solved | false |
| 11 | [2016 Dec, Q1(b)(i-ii)](CIVL1113-2016-dec-mechanics.pdf#page=1) | Draw signed SFD and tensile-side BMD for a three-hinged frame with opposite applied moments either side of the crown hinge. | Not solved | false |
| 12 | [2015 Dec, Q2(a)](CIVL1113-2015-dec-mechanics.pdf#page=2) | Sketch AFD, SFD and tension-side BMD for a simply supported rigid frame under horizontal loading. | Not solved | false |

## Bending stress and section sizing

**12 rows · 10 distinct papers.** Find centroid and second moment of area; obtain the critical bending moment and any axial force; evaluate extreme normal stresses; enforce the governing allowable stress or solve for section/load.
Reference: Lectures 4–5.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2025 Dec, Q1(a)(ii)](CIVL1113-2025-dec-mechanics.pdf#page=2) | Choose the smallest square solid beam section satisfying the flexural stress limit. | Not solved | false |
| 2 | [2025 Dec, Q1(b)(ii)](CIVL1113-2025-dec-mechanics.pdf#page=2) | Determine maximum compressive normal stress in the box-section frame, including the internal axial force where applicable. | Not solved | false |
| 3 | [2022 May, Q2(c)](CIVL1113-2022-may-mechanics.pdf#page=1) | Find extreme tensile/compressive normal stress from the combination of axial force and bending moment. | Not solved | true: 2, 9 |
| 4 | [2020 Dec, Q3(b)](CIVL1113-2020-dec-mechanics.pdf#page=2) | For the same circular bar, locate and calculate maximum bending stress. | Not solved | false |
| 5 | [2020 May, Q2(b)](CIVL1113-2020-may-mechanics.pdf#page=2) | For the same circular bar, locate and calculate maximum bending stress. | Not solved | false |
| 6 | [2019 May, Q2(d)](CIVL1113-2019-may-mechanics.pdf#page=1) | Determine the largest additional central point load before tensile cracking and identify where the first crack occurs. | Not solved | false |
| 7 | [2019 May, Q3(c)](CIVL1113-2019-may-mechanics.pdf#page=2) | Calculate maximum tensile and compressive bending stresses and their positions in the T-section beam. | Not solved | false |
| 8 | [2017 May, Q2(c)](CIVL1113-2017-may-mechanics.pdf#page=1) | Find maximum beam stress and its location for the beam-truss assembly. | Not solved | false |
| 9 | [2016 Dec, Q2(c)](CIVL1113-2016-dec-mechanics.pdf#page=1) | Find maximum tensile and compressive stresses and their positions in the T-beam under combined axial force and bending. | Not solved | false |
| 10 | [2015 Dec, Q1](CIVL1113-2015-dec-mechanics.pdf#page=2) | Find allowable UDL for an overhanging beam with unequal I-section flanges and different tension/compression limits. | Not solved | true: 1, 6, 7, 8, 11, 12 |
| 11 | [2013 Dec, Q2(a-c)](CIVL1113-2013-dec-mechanics.pdf#page=2) | Locate the T-section centroid, find maximum allowable UDL from the tensile limit, and calculate the largest flange bending stress. | Not solved | false |
| 12 | [2011 May, Q1(a,b,d)](CIVL1113-2011-may-mechanics.pdf#page=2) | Express box-section second moment of area, size its width for a point load, and find load capacity for a specified width. | Not solved | false |

## Axial deformation and compatibility

**10 rows · 7 distinct papers.** Find axial forces, evaluate deformation using the local EA, and impose support or rigid-member compatibility to obtain the unknown force/stress/displacement.
Reference: Lecture 2.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2024 Dec, Q3(ii)](CIVL1113-2024-dec-mechanics.pdf#page=3) | Calculate the column end displacement at the allowable load. | Not solved | true: 2 |
| 2 | [2023 Dec, Q3(b)(ii)](CIVL1113-2023-dec-mechanics.pdf#page=3) | Calculate column shortening at the allowable load obtained from Euler buckling. | Not solved | false |
| 3 | [2019 May, Q2(b)](CIVL1113-2019-may-mechanics.pdf#page=1) | Find elongation of the two suspension wires under the beam's gravity load. | Not solved | false |
| 4 | [2019 May, Q3(d-e)](CIVL1113-2019-may-mechanics.pdf#page=2) | Find the brace contraction, then use rigid-beam kinematics to obtain end displacement when beam bending stiffness is infinite. | Not solved | true: 3, 8 |
| 5 | [2017 Dec, Q2(a)(ii)](CIVL1113-2017-dec-mechanics.pdf#page=1) | Calculate displacements of the free end and loaded junction of a two-material axial bar. | Not solved | false |
| 6 | [2017 Dec, Q2(b)(i)](CIVL1113-2017-dec-mechanics.pdf#page=1) | For an axial bar fixed at both ends with equal elastic moduli, find the AFD and junction displacement. | Not solved | false |
| 7 | [2017 Dec, Q2(b)(ii)](CIVL1113-2017-dec-mechanics.pdf#page=1) | For an axial bar fixed at both ends with unequal elastic moduli, find the AFD and junction displacement. | Not solved | true: 6, 9 |
| 8 | [2017 May, Q2(d)](CIVL1113-2017-may-mechanics.pdf#page=1) | Calculate displacement of connection C using the axial deformation of its truss support. | Not solved | false |
| 9 | [2016 May, Q3(a)](CIVL1113-2016-may-mechanics.pdf#page=3) | Find stresses in two dissimilar concentric bars between fixed supports after the support separation is reduced. | Not solved | false |
| 10 | [2014 Dec, Q1(a)](CIVL1113-2014-dec-mechanics.pdf#page=2) | Calculate total change in length of two connected tapered circular bars under end and intermediate axial loads. | Not solved | false |

## Beam combined stresses and failure checks

**8 rows · 8 distinct papers.** Obtain the section forces; calculate normal and transverse-shear stresses at candidate points; apply the named Tresca or von Mises criterion; compare all relevant sections and points.
Reference: Lectures 4–7 and 10.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2026 May, Q2(a)(i-ii)](CIVL1113-2026-may-mechanics.pdf#page=2) | Find tensile/compressive normal stresses and maximum shear in the given beam section, then check Tresca safety. | Not solved | true: 3, 8 |
| 2 | [2025 Dec, Q2(a)(i-ii)](CIVL1113-2025-dec-mechanics.pdf#page=2) | Find maximum normal/shear stresses in a point-loaded simply supported beam and check von Mises safety. | Not solved | false |
| 3 | [2025 May, Q2(a)(i-ii)](CIVL1113-2025-may-mechanics.pdf#page=2) | Combine self-weight bending, transverse shear and axial tension in a thin-web cantilever; check strength using Tresca. | Not solved | false |
| 4 | [2024 Dec, Q2(a)(i-ii)](CIVL1113-2024-dec-mechanics.pdf#page=2) | Find maximum bending/shear stresses in a UDL-loaded cantilever I-beam and evaluate von Mises safety. | Not solved | true: 2, 5, 6, 7 |
| 5 | [2024 May, Q2(a)](CIVL1113-2024-may-mechanics.pdf#page=2) | Convert beam self-weight to loading, determine combined bending/shear stresses and check a slender-web cantilever with von Mises. | Not solved | false |
| 6 | [2023 Dec, Q2(a)(i-ii)](CIVL1113-2023-dec-mechanics.pdf#page=2) | Find maximum normal/shear stresses of an axially loaded cantilever I-beam and check von Mises safety, including its flange/web junction. | Not solved | false |
| 7 | [2022 May, Q2(e)](CIVL1113-2022-may-mechanics.pdf#page=1) | Evaluate von Mises safety at top, bottom and centre on both sides of a critical section and locate the governing point. | Not solved | false |
| 8 | [2016 Dec, Q2(d)](CIVL1113-2016-dec-mechanics.pdf#page=1) | Check the T-beam against the Tresca allowable-shear criterion and locate the maximum shear. | Not solved | false |

## Beam deflection by integration or compatibility

**8 rows · 8 distinct papers.** Obtain M(x); use the elastic-curve equation or a suitable superposition; impose boundary/continuity conditions and any compatibility constraint; find the requested deflection, rotation or unknown load.
Reference: Lecture 12.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2021 May, Q1(a–b)](CIVL1113-2021-may-mechanics.pdf#page=2) | Derive the elastic-curve equations for a cantilever with partial UDL and a tip force, then determine its tip deflection. | Not solved | true: 6, 7, 8 |
| 2 | [2018 May, Q3(a)](CIVL1113-2018-may-mechanics.pdf#page=1) | Express the central point load on a simply supported beam in terms of its central deflection, EI and span. | Not solved | false |
| 3 | [2017 Dec, Q3(a)(ii)](CIVL1113-2017-dec-mechanics.pdf#page=2) | Find the cantilever-column tip deflection and the maximum positive bending stress and its position. | Not solved | false |
| 4 | [2012 Dec, Q2(b)](CIVL1113-2012-dec-mechanics.pdf#page=3) | Find the prop reaction of a propped cantilever by enforcing zero vertical movement at B. | Not solved | false |
| 5 | [2012 May, Q2(a-c)](CIVL1113-2012-may-mechanics.pdf#page=3) | Find reactions, derive the entire elastic curve by Macaulay's method, and choose the point load that makes midspan deflection zero. | Not solved | true: 8 |
| 6 | [2011 May, Q2(a-c)](CIVL1113-2011-may-mechanics.pdf#page=3) | Find cantilever reactions, derive the elastic curve by the differential-equation method, and evaluate end deflections. | Not solved | false |
| 7 | [2010 May, Q1(a-d)](CIVL1113-2010-may-mechanics.pdf#page=2) | Find reactions, derive the deflection curve of a cantilever under linearly varying load, and obtain end deflections and rotations. | Not solved | false |
| 8 | [2009 May, Q1(a-c)](CIVL1113-2009-may-mechanics.pdf#page=2) | Find reactions, form a Macaulay bending-moment expression, and calculate deflection at C. | Not solved | false |

## Coupled-member deflection and compatibility

**8 rows · 4 distinct papers.** Write the bending and axial/spring deformations of each member; enforce joint displacement compatibility and equilibrium; solve the load-sharing/deformation system.
Reference: Lectures 2 and 12.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2019 May, Q2(c)](CIVL1113-2019-may-mechanics.pdf#page=1) | Sketch the suspended beam deformation and calculate central deflection, including support-wire extension. | Not solved | true: 8 |
| 2 | [2018 May, Q3(b)](CIVL1113-2018-may-mechanics.pdf#page=1) | Derive the central load-deflection relation when a linear spring supports the beam midpoint. | Not solved | false |
| 3 | [2018 May, Q3(c)](CIVL1113-2018-may-mechanics.pdf#page=2) | Derive the central load-deflection relation when a finite-axial-stiffness vertical rod supports the midpoint; neglect rod buckling. | Not solved | true: 2, 4, 5 |
| 4 | [2018 May, Q3(d)](CIVL1113-2018-may-mechanics.pdf#page=2) | Derive the load-deflection relation for two identical simply supported beams linked at their midpoints by an axially rigid rod. | Not solved | false |
| 5 | [2018 May, Q3(e)](CIVL1113-2018-may-mechanics.pdf#page=2) | Repeat the two-beam midpoint load-deflection relation for a rod with finite axial stiffness. | Not solved | false |
| 6 | [2017 Dec, Q3(b)(i)](CIVL1113-2017-dec-mechanics.pdf#page=2) | For two cantilever columns linked at their tops by a truss element with zero axial stiffness, draw BMD and calculate loaded-top deflection. | Not solved | false |
| 7 | [2017 Dec, Q3(b)(ii)](CIVL1113-2017-dec-mechanics.pdf#page=2) | Repeat BMD and loaded-top deflection for the two-column system when the linking truss has infinite axial stiffness. | Not solved | false |
| 8 | [2017 May, Q2(e)](CIVL1113-2017-may-mechanics.pdf#page=1) | Combine support-member movement and beam bending to determine the deflection at B. | Not solved | false |

## Circular-shaft torsion

**7 rows · 7 distinct papers.** Obtain internal torque and the circular-section torsional property; find stress/strain and twist; enforce the stated stress, strain or twist restriction. Distinguish solid/thick-wall and thin-wall assumptions.
Reference: Lecture 8.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2026 May, Q3(a)](CIVL1113-2026-may-mechanics.pdf#page=3) | Find the maximum rod diameter consistent with a specified end rotation and allowable shear strain. | Not solved | false |
| 2 | [2025 May, Q1(a)(i-ii)](CIVL1113-2025-may-mechanics.pdf#page=2) | Find maximum shear stress and free-end twist of a thick-walled circular tube, using a nonuniform shear-stress distribution. | Not solved | true: 4, 5, 6, 7 |
| 3 | [2024 May, Q3(a)](CIVL1113-2024-may-mechanics.pdf#page=2) | Choose the minimum solid-shaft diameter satisfying both allowable shear stress and allowable twist per unit length. | Not solved | true: 1 |
| 4 | [2023 Dec, Q3(a)(i-ii)](CIVL1113-2023-dec-mechanics.pdf#page=3) | Find maximum shaft shear stress and the angle of twist at C for a solid circular shaft with torque at an interior point. | Not solved | false |
| 5 | [2022 May, Q3(a)(i-ii)](CIVL1113-2022-may-mechanics.pdf#page=1) | Calculate shear stress and angle of twist of a thin-walled hollow circular cantilever shaft. | Not solved | false |
| 6 | [2020 Dec, Q3(a)](CIVL1113-2020-dec-mechanics.pdf#page=2) | For a circular bar under end torque and bending moment, locate and calculate maximum torsional shear stress. | Not solved | false |
| 7 | [2020 May, Q2(a)](CIVL1113-2020-may-mechanics.pdf#page=2) | For a circular bar under end torque and bending moment, locate and calculate maximum torsional shear stress. | Not solved | false |

## Layered-beam strength and load sharing

**7 rows · 3 distinct papers.** Determine load sharing for the specified layered-beam connection; compute each beam's extreme bending stress; find the allowable total load and governing surface.
Reference: Lectures 4–5 and 12.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2020 Dec, Q1(c)](CIVL1113-2020-dec-mechanics.pdf#page=2) | Find the allowable tip load and failure surface of the unbonded two-beam system using the allowable normal stress. | Not solved | true: 4, 6 |
| 2 | [2020 Dec, Q1(d)](CIVL1113-2020-dec-mechanics.pdf#page=2) | Find the allowable tip load and failure surface of the end-pinned two-beam system. | Not solved | true: 5, 7 |
| 3 | [2020 Dec, Q1(e)](CIVL1113-2020-dec-mechanics.pdf#page=2) | Compare the conclusions from the unbonded and end-pinned layered-beam cases. | Not solved | false |
| 4 | [2020 May, Q1(c)](CIVL1113-2020-may-mechanics.pdf#page=2) | Find the allowable tip load and failure surface of the unbonded two-beam system using the allowable normal stress. | Not solved | false |
| 5 | [2020 May, Q1(d)](CIVL1113-2020-may-mechanics.pdf#page=2) | Find the allowable tip load and failure surface of the end-pinned two-beam system. | Not solved | false |
| 6 | [2018 May, Q2(c)](CIVL1113-2018-may-mechanics.pdf#page=1) | Find the allowable tip load and failure surface for the two stacked, unbonded beams using the allowable normal stress. | Not solved | false |
| 7 | [2018 May, Q2(d)](CIVL1113-2018-may-mechanics.pdf#page=1) | Find the allowable tip load and failure surface when the two beams are pinned together at the loaded end. | Not solved | false |

## Failure criteria for a plane-stress element

**6 rows · 6 distinct papers.** Use the signed normal/shear stress state, including the zero out-of-plane principal stress; evaluate the named yield criterion and compare with the allowable/yield stress.
Reference: Lectures 9–10.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2026 May, Q2(b)(ii)](CIVL1113-2026-may-mechanics.pdf#page=2) | Check von Mises safety of the specified plane-stress point. | Not solved | true: 2, 3, 4, 5 |
| 2 | [2025 Dec, Q2(b)(ii)](CIVL1113-2025-dec-mechanics.pdf#page=2) | Evaluate von Mises safety of the plane-stress point. | Not solved | false |
| 3 | [2025 May, Q2(b)(ii)](CIVL1113-2025-may-mechanics.pdf#page=2) | Check von Mises safety of the given stress state using its yield strength. | Not solved | false |
| 4 | [2024 Dec, Q2(b)(ii)](CIVL1113-2024-dec-mechanics.pdf#page=2) | Check von Mises safety of the plane-stress point against the given yield strength. | Not solved | false |
| 5 | [2024 May, Q2(b)(ii)](CIVL1113-2024-may-mechanics.pdf#page=2) | Check the given plane-stress state using the von Mises criterion and the allowable equivalent stress. | Not solved | false |
| 6 | [2023 Dec, Q2(b)(ii)](CIVL1113-2023-dec-mechanics.pdf#page=3) | Check the specified plane-stress element against the Tresca criterion using its uniaxial yield stress. | Not solved | false |

## Layered-beam deflection and load sharing

**6 rows · 3 distinct papers.** Identify whether the two beams are unbonded or joined at the loaded end; use their bending stiffnesses and displacement compatibility to determine load sharing and tip movement.
Reference: Lectures 5 and 12.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2020 Dec, Q1(a)](CIVL1113-2020-dec-mechanics.pdf#page=2) | Calculate tip deflection for two stacked, unbonded cantilever beams with upper/lower thicknesses 4h and h. | Not solved | true: 3, 5 |
| 2 | [2020 Dec, Q1(b)](CIVL1113-2020-dec-mechanics.pdf#page=2) | Calculate tip deflection for the same two beams when pinned together at their loaded ends. | Not solved | true: 4, 6 |
| 3 | [2020 May, Q1(a)](CIVL1113-2020-may-mechanics.pdf#page=2) | Calculate tip deflection for two stacked, unbonded cantilever beams with upper/lower thicknesses 3h and h. | Not solved | false |
| 4 | [2020 May, Q1(b)](CIVL1113-2020-may-mechanics.pdf#page=2) | Calculate tip deflection for the same two beams when pinned together at their loaded ends. | Not solved | false |
| 5 | [2018 May, Q2(a)](CIVL1113-2018-may-mechanics.pdf#page=1) | Calculate tip deflection for two stacked, unbonded cantilever beams of thickness h and 3h. | Not solved | false |
| 6 | [2018 May, Q2(b)](CIVL1113-2018-may-mechanics.pdf#page=1) | Calculate tip deflection for the same two cantilever beams when pinned together at the loaded end. | Not solved | false |

## Beam shear stress and connector design

**3 rows · 3 distinct papers.** Find V, section I and first moment Q; evaluate shear stress or shear flow; for built-up members, relate connector force/capacity to spacing and quantity.
Reference: Lectures 6–7.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2015 May, Q3](CIVL1113-2015-may-mechanics.pdf#page=3) | Design longitudinal bolt spacing for a made-up timber box beam and count the bolts subject to installation-spacing restrictions. | Not solved | true: 2 |
| 2 | [2014 Dec, Q3(a)](CIVL1113-2014-dec-mechanics.pdf#page=3) | Choose bolt diameter and spacing to join the T-beam flange and web without exceeding allowable bolt shear. | Not solved | false |
| 3 | [2011 May, Q1(e)](CIVL1113-2011-may-mechanics.pdf#page=2) | Calculate maximum section shear stress in the welded box-section beam under the specified central load. | Not solved | false |

## Euler buckling and material-failure comparison

**3 rows · 3 distinct papers.** Determine axis-specific elastic buckling loads and compressive material limits; compare them, check applicability, and identify the governing failure mode.
Reference: Lecture 11.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2021 May, Q2(a–b)](CIVL1113-2021-may-mechanics.pdf#page=2) | Find the maximum compressive load of a pin-ended I-section column with midpoint lateral restraint in one plane only; determine whether buckling or material failure governs. | Not solved | false |
| 2 | [2020 Dec, Q2(a–b)](CIVL1113-2020-dec-mechanics.pdf#page=2) | Find the maximum compressive load of a rectangular vertical bar fixed at its base and pin-connected to a long horizontal beam; determine whether buckling or material failure governs. | Not solved | true: 3 |
| 3 | [2020 May, Q3(a–b)](CIVL1113-2020-may-mechanics.pdf#page=2) | Find the maximum compressive load of a rectangular vertical bar fixed at its base and pin-connected to a long horizontal beam; determine whether buckling or material failure governs. | Not solved | false |

## Plane-stress transformation derivations

**3 rows · 3 distinct papers.** Start from equilibrium of a cut stress element or the supplied transformation equations; derive the requested expression, circle identity or angular relationship.
Reference: Lecture 9.

**Priority note:** The three rows derive different results: the circle equation, principal/shear-plane results, and the original transformation equation.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2012 Dec, Q3(a)](CIVL1113-2012-dec-mechanics.pdf#page=3) | Derive the equation of Mohr's circle from the stress-transformation equations. | Not solved | false |
| 2 | [2012 May, Q3(a-b)](CIVL1113-2012-may-mechanics.pdf#page=3) | Derive maximum/minimum principal stresses and prove that maximum-shear planes are 45 degrees to principal planes. | Not solved | false |
| 3 | [2011 May, Q3](CIVL1113-2011-may-mechanics.pdf#page=4) | Derive the transformed normal-stress equation from first principles using the original and rotated stress elements. | Not solved | false |

## Buckling and yield transition concepts

**2 rows · 2 distinct papers.** Relate the buckling mechanism to slenderness, yield limits or changing member stiffness; sketch/explain the requested trend.
Reference: Lecture 11.

**Priority note:** Changing frame axial rigidity and sketching the Euler/yield transition are different conceptual tasks.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2017 May, Q3(b)](CIVL1113-2017-may-mechanics.pdf#page=1) | Explain how the two frame buckling loads change as member axial rigidity is reduced from infinity to zero. | Not solved | false |
| 2 | [2009 May, Q3(c)](CIVL1113-2009-may-mechanics.pdf#page=3) | Plot critical stress against slenderness, including the Euler branch and the yield-stress limit. | Not solved | false |

## Composite-section bending

**2 rows · 2 distinct papers.** Use stiffness compatibility and the correct composite/noncomposite model; locate the neutral axis or equivalent section; compare stress limits in both materials to find the allowable load.
Reference: Lecture 5.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2015 May, Q2(a)](CIVL1113-2015-may-mechanics.pdf#page=2) | Find allowable UDL for an overhanging composite beam using the different elastic moduli and stress limits. | Not solved | true: 2 |
| 2 | [2014 Dec, Q2(a-b)](CIVL1113-2014-dec-mechanics.pdf#page=3) | Compare allowable UDL for stacked dissimilar-material beams with and without composite action. | Not solved | false |

## Truss equilibrium and member forces

**2 rows · 2 distinct papers.** Use support equilibrium and joint/section equilibrium to determine every axial member force and its tension/compression sign.
Reference: Lectures 1–3.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2021 Dec, Q3(a)](CIVL1113-2021-dec-mechanics.pdf#page=2) | Find every bar force in two square trusses with different diagonal arrangements under horizontal load. | Not solved | true: 2 |
| 2 | [2016 Dec, Q3(a)](CIVL1113-2016-dec-mechanics.pdf#page=1) | Find every bar force in each of two square trusses with opposite diagonal arrangements, in terms of the applied horizontal load. | Not solved | false |

## Beam kinematics and differential-equation derivations

**2 rows · 1 distinct papers.** Use beam geometry and small-deformation assumptions to derive the printed curvature/rotation or elastic-curve relationship.
Reference: Lectures 4 and 12.

**Priority note:** Curvature/rotation kinematics and deriving the elastic-curve equation are connected but distinct derivation tasks.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2012 Dec, Q1(a)](CIVL1113-2012-dec-mechanics.pdf#page=2) | Derive the relationship between curvature and rotation gradient and explain the physical meaning of curvature. | Not solved | false |
| 2 | [2012 Dec, Q2(a)](CIVL1113-2012-dec-mechanics.pdf#page=3) | Derive the elastic-curve differential equation dÂ²v/dxÂ² = M/(EI) from first principles. | Not solved | false |

## Indeterminate compound-shaft torsion

**2 rows · 1 distinct papers.** Combine torque equilibrium with compatible end rotations; distribute torque between different GJ/L segments; enforce material stress limits and optimise the requested length ratio.
Reference: Lecture 8.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2021 Dec, Q1(a)](CIVL1113-2021-dec-mechanics.pdf#page=2) | Find the maximum applied junction torque in a bronze-steel compound shaft restrained by rigid end supports. | Not solved | true: 2 |
| 2 | [2021 Dec, Q1(b)](CIVL1113-2021-dec-mechanics.pdf#page=2) | Choose the bronze/steel length ratio so both shaft materials reach their allowable shear stress together, and find the corresponding torque. | Not solved | false |

## Buckling-axis identification

**1 rows · 1 distinct papers.** Compare centroidal/principal section stiffnesses under the stated equal end restraints; draw the likely weak-axis buckling direction.
Reference: Lectures 5 and 11.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2016 May, Q3(c)](CIVL1113-2016-may-mechanics.pdf#page=4) | Identify and draw the expected buckling axis for rectangular, T, I and equal-angle cross-sections. | Not solved | false |

## Curvature from bending moment

**1 rows · 1 distinct papers.** Evaluate the relevant M and section EI, then obtain curvature from the elastic bending relation.
Reference: Lectures 4 and 12.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2011 May, Q1(c)](CIVL1113-2011-may-mechanics.pdf#page=2) | Determine the beam curvature for the section and loading obtained in the preceding part. | Not solved | false |

## Deformation sketches from support constraints

**1 rows · 1 distinct papers.** Use the support displacement constraints and symmetry to sketch a physically compatible deformed shape.
Reference: Lecture 12.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2019 May, Q2(e)](CIVL1113-2019-may-mechanics.pdf#page=1) | Sketch the beam deformation after adding a third, infinitely stiff suspension wire at midspan. | Not solved | false |

## Moment-area theorem explanation

**1 rows · 1 distinct papers.** State what the area of the M/EI diagram represents between two beam sections and illustrate the rotation relationship.
Reference: Lecture 12.

| # | Source | Question description | Status | Priority status |
| ---: | --- | --- | --- | --- |
| 1 | [2009 May, Q1(d)](CIVL1113-2009-may-mechanics.pdf#page=2) | State the First Moment-Area Theorem and illustrate it with suitable diagrams. | Not solved | false |

## Paper and comment inventory

| Moodle session label | Paper | Source | Note |
| --- | --- | --- | --- |
| 2009 May | [PDF](CIVL1113-2009-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302661) |  |
| 2010 May | [PDF](CIVL1113-2010-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302662) |  |
| 2011 May | [PDF](CIVL1113-2011-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302663) |  |
| 2012 May | [PDF](CIVL1113-2012-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302664) |  |
| 2012 Dec | [PDF](CIVL1113-2012-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302665) |  |
| 2013 Dec | [PDF](CIVL1113-2013-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302666) |  |
| 2014 Dec | [PDF](CIVL1113-2014-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302667) |  |
| 2015 May | [PDF](CIVL1113-2015-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302668) |  |
| 2015 Dec | [PDF](CIVL1113-2015-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302669) |  |
| 2016 May | [PDF](CIVL1113-2016-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302670) |  |
| 2016 Dec | [PDF](CIVL1113-2016-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302671) |  |
| 2017 May | [PDF](CIVL1113-2017-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302672) |  |
| 2017 Dec | [PDF](CIVL1113-2017-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302673) |  |
| 2018 May | [PDF](CIVL1113-2018-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302674) |  |
| 2018 Dec | [PDF](CIVL1113-2018-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302675) | Duplicate of 2018 May; excluded from recurrence |
| 2019 May | [PDF](CIVL1113-2019-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302676) |  |
| 2020 May | [PDF](CIVL1113-2020-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302677) |  |
| 2020 Dec | [PDF](CIVL1113-2020-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302678) |  |
| 2021 May | [PDF](CIVL1113-2021-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302679) |  |
| 2021 Dec | [PDF](CIVL1113-2021-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302680) |  |
| 2022 May | [PDF](CIVL1113-2022-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302681) | Date label uncertain; no dated cover in extract |
| 2023 Dec | [PDF](CIVL1113-2023-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302683) |  |
| 2024 May | [PDF](CIVL1113-2024-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302684) |  |
| 2024 Dec | [PDF](CIVL1113-2024-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302686) |  |
| 2025 May | [PDF](CIVL1113-2025-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302688) |  |
| 2025 Dec | [PDF](CIVL1113-2025-dec-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302690) |  |
| 2026 May | [PDF](CIVL1113-2026-may-mechanics.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302699) |  |

| Session | Lecturer comments | Source |
| --- | --- | --- |
| 2024 May | [PDF](CIVL1113-2024-may-comments.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302685) |
| 2024 Dec | [PDF](CIVL1113-2024-dec-comments.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302687) |
| 2025 May | [PDF](CIVL1113-2025-may-comments.pdf) | [Moodle](https://moodle.hku.hk/mod/resource/view.php?id=4302689) |

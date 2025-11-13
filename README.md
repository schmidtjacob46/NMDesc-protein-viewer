🧬 NMDesc Protein Feature & Variant Viewer

Interactive, browser-based visualization tool for exploring protein features and overlaying custom variants used in the NMDesc project.
Hosted via GitHub Pages for easy access without installing any dependencies.

🔗 Live Viewer:
https://schmidtjacob46.github.io/NMDesc-protein-viewer/protein_features_viewer_with_variants.html

🚀 Features
🧭 Protein Navigation

Fast dropdown selection for 20,000+ UniProt/Ensembl proteins

Search-as-you-type filtering

🧩 Feature Visualization

Tracks included:

Protein domains

UniProt protein features

PTMs (phosphorylation, acetylation, ubiquitination, etc.)

SLiMs (ELM)

MORFs (MFIB)

NLS/NES signals (NLSdb)

Low-complexity sequences (LCSs)

Backbone domains (InterPro)

Toggle: Show/Hide single-site features (PTMs + single-site PFs)

🎯 Variant Overlay

Supports:

A123T

123A>T

123

comma/space-separated lists

Variants appear as:

vertical red markers

clickable “variant tags” above the plot

hover text with standardized formatting

🔍 Plot Interaction

pan/zoom

reset zoom

rich hover annotations

📁 Repository Structure
NMDesc-protein-viewer/
│
├── docs/
│   ├── protein_features_viewer_with_variants.html   # Live interactive viewer
│   └── protein_data/                                # ~20k JSON protein annotation files
│
├── README.md
├── .gitignore
└── LICENSE (MIT)


GitHub Pages publishes from the docs/ directory.

📊 Data Sources
(Integrated directly from Banani et al., Supplemental Table S4)

All protein features displayed in this viewer were parsed directly from:

Banani et al., “Genetic Variation Associated with Condensate Dysregulation in Disease.”
Supplemental Information — Table S4
(This workbook contains all canonical protein features, condensate-associated annotations, and curated linear motifs used in the study.)

The following sections of Table S4 correspond to the tracks in the viewer:

A. Human Protein Sequences

Used for:

Protein backbone length

ID mapping

Amino acid coordinate system

Fields:

Protein name

UniProt ID

Sequence

B. Mapped Protein Features (Integrated from Annotation Databases)
Viewer Track	Source Section	Database
Protein Features	B	UniProt
Domains	B	InterPro
SLiMs	B	ELM
MORFs	B	MFIB
PTMs	B	PhosphoSitePlus
NLSs/NESs	B	NLSdb

Section B describes:

structural and functional features

interacting regions

PTMs

SLiMs

MORFs

nuclear signal sequences

G. LCS Mapping Across the Proteome

Used for:

LCS track (green blocks)

Section includes:

low-complexity sequences associated with condensate formation

H. Pathogenic Mutations Affecting Condensate-Promoting Features

(Optional overlay when variants are loaded)

Fields:

MIDs

LCSs

Pathogenic mutations

Disease + cancer associations

These data are used only if the user overlays variants.

✔ Summary Table
Track (Viewer)	Table S4 Section	Primary Database
Backbone	A	UniProt
Domains	B	InterPro
Protein Features	B	UniProt
SLiMs	B	ELM
MORFs	B	MFIB
PTMs	B	PhosphoSitePlus
NLSs/NESs	B	NLSdb
LCSs	G	LCS mapping (Banani)
Mutations (optional)	C, D, H	As included in Table S4
🔧 Technical Notes

Pure static viewer (HTML + JS + Plotly), no backend required

Loads only the selected protein’s JSON file

Supports ~600 MB of annotations (20,145 proteins)

Designed to be stable on GitHub Pages

🌐 Hosting

GitHub Pages configuration:

Branch: main

Folder: docs/

Updates deploy automatically upon pushing to main.

📥 Updating the Viewer

Run the Jupyter notebook that generates:

protein_features_viewer_with_variants.html

All updated JSONs

Replace files in docs/

Run:

git add docs/
git commit -m "Update viewer"
git push

📜 License

Released under the MIT License.

👥 Contact

For questions or collaboration:

Jake Schmidt
UTHealth Houston — Coban Akdemir Lab
GitHub: schmidtjacob46

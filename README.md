# 🧬 NMDesc Protein Feature & Variant Viewer

Interactive, browser-based visualization tool for exploring protein features and overlaying custom variants used in the **NMDesc** project.  
Hosted via **GitHub Pages** for easy access without installing any dependencies.

🔗 **Live Viewer:**  
https://schmidtjacob46.github.io/NMDesc-protein-viewer/protein_features_viewer_with_variants.html

---

# 📁 Repository Contents

```
NMDesc-protein-viewer/
│
├── docs/
│   ├── protein_features_viewer_with_variants.html   # Live interactive viewer
│   └── protein_data/                                # ~20k JSON protein annotation files
│
├── generate_protein_viewer_data.ipynb                   # Notebook used to generate HTML + JSONs
├── NIHMS1818854-supplement-2.xlsx                   # Supplemental Table S4 from Banani et al.
├── README.md
├── LICENSE
└── .gitignore
```

---

# 🚀 Features

### 🧭 Protein Navigation
- Fast dropdown selection for **20,000+ UniProt/Ensembl proteins**
- Search-as-you-type filtering

### 🧩 Feature Visualization
Tracks included:
- Protein domains  
- UniProt features  
- PTMs (e.g., phosphorylation)  
- SLiMs (ELM)  
- MORFs (MFIB)  
- NLS/NES (NLSdb)  
- Low-complexity sequences  
- Backbone domains  

Toggle available: **Show/Hide single-site features**

### 🎯 Variant Overlay
Accepts:
- `A123T`
- `123A>T`
- `123`
- comma‑ or space‑separated lists

Displayed as:
- vertical red markers  
- clickable variant “chips”  
- hover-text annotation  

### 🔍 Plot Interaction
- pan / zoom  
- reset zoom  
- detailed hover information  

---

# 📊 Data Sources  
### *(From Banani et al., Supplemental Table S4 — primary source)*

All features were parsed from:

**Banani SF, Afeyan LK, Hawken SW, Henninger JE, et al.**  
**Genetic Variation Associated with Condensate Dysregulation in Disease.**  
*Cell.* 2023;184(2):341–359.e25.  
doi:10.1016/j.cell.2023.01.013  
PMC 9339523  
https://pmc.ncbi.nlm.nih.gov/articles/PMC9339523/

The supplemental workbook (**NIHMS1818854-supplement-2.xlsx**) provides:
- canonical protein sequences  
- mapped UniProt features  
- InterPro domains  
- ELM SLiMs  
- MFIB MORFs  
- PhosphoSitePlus PTMs  
- NLSdb nuclear localization/export signals  
- LCS regions  
- pathogenic mutations affecting condensate-promoting features  

---

## ✔ Breakdown of Table S4 Sections Used

### **A. Human Protein Sequences**
Backbone length, ID mapping, sequence.

### **B. Mapped Protein Features**
Includes:
- UniProt features  
- InterPro domains  
- ELM SLiMs  
- MFIB MORFs  
- PhosphoSitePlus PTMs  
- NLSdb NLS/NES  

### **G. LCS Mapping Across the Proteome**
Used for LCS track.

### **H. Pathogenic Mutations Affecting Condensate-Promoting Features**
Optional overlay used when user enters variants.

---

## ✔ Summary Table

| Viewer Track | Table S4 Section | Source Database |
|--------------|------------------|-----------------|
| Backbone | A | UniProt |
| Domains | B | InterPro |
| Protein Features | B | UniProt |
| SLiMs | B | ELM |
| MORFs | B | MFIB |
| PTMs | B | PhosphoSitePlus |
| NLS/NES | B | NLSdb |
| LCS | G | Banani LCS mapping |
| Mutations (optional) | C/D/H | Provided in workbook |

---

# 🧪 Reproducing the Data (Notebook Workflow)

The file **`generate_protein_viewer_data.ipynb`** contains all preprocessing steps to regenerate:
- **protein_data/*.json**  
- **protein_features_viewer_with_variants.html**

Workflow summary:
1. Load `NIHMS1818854-supplement-2.xlsx`  
2. Parse Table S4 sections  
3. Normalize annotation tracks  
4. Build JSON files (one per protein)  
5. Generate final viewer HTML with embedded JavaScript  

This provides full reproducibility for all files hosted in `/docs`.

---

# 🌐 Hosting via GitHub Pages

GitHub Pages configuration:
- **Branch:** `main`
- **Folder:** `docs/`

The site updates automatically when files inside `/docs` are modified.

---

# 📥 Updating the Viewer

To update the public viewer:

```
git add docs/
git commit -m "Update viewer"
git push
```

Deployment finishes in ~1–2 minutes.

---

# 📜 License
This project is released under the **MIT License**.

---

# 👥 Contact

**Jake Schmidt**  
UTHealth Houston — Coban Akdemir Lab  
GitHub: schmidtjacob46

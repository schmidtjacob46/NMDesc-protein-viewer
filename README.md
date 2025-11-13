# 🧬 NMDesc Protein Feature & Variant Viewer

Interactive, browser-based visualization tool for exploring protein features and overlaying custom variants used in the **NMDesc** project.  
Hosted via **GitHub Pages** for easy access without installing any dependencies.

🔗 **Live Viewer:**  
https://schmidtjacob46.github.io/NMDesc-protein-viewer/protein_features_viewer_with_variants.html

---

## 🚀 Features

### 🧭 Protein Navigation
- Fast dropdown selection for **20,000+ UniProt/Ensembl proteins**
- Search-as-you-type filtering

### 🧩 Feature Visualization
Tracks included:
- Protein domains  
- UniProt protein features  
- PTMs  
- SLiMs  
- MORFs  
- NLS/NES signals  
- Low-complexity sequences  
- Backbone domains  

Toggle: **Show/Hide single-site features**

### 🎯 Variant Overlay
Supports:
- A123T  
- 123A>T  
- 123  
- comma/space-separated lists  

Variants appear as:
- vertical markers  
- clickable variant chips  
- hover-text annotation  

### 🔍 Plot Interaction
- pan/zoom  
- reset zoom  
- high-quality hover labels  

---

## 📁 Repository Structure

```
NMDesc-protein-viewer/
│
├── docs/
│   ├── protein_features_viewer_with_variants.html
│   └── protein_data/
│
├── README.md
├── .gitignore
└── LICENSE
```

GitHub Pages publishes from the `docs/` directory.

---

# 📊 Data Sources  
### *(Integrated directly from Banani et al., Supplemental Table S4 — primary source)*

All protein features displayed in this viewer were parsed directly from the supplemental workbook associated with:

**Banani SF, Afeyan LK, Hawken SW, Henninger JE, Dall’Agnese A, Clark VE, Platt JM, Oksuz Ö, Hannett NE, Sagi I, Lee TI, Young RA.**  
**Genetic Variation Associated with Condensate Dysregulation in Disease.**  
*Cell.* 2023;184(2):341–359.e25.  
doi:10.1016/j.cell.2023.01.013  
PMC: 9339523  
https://pmc.ncbi.nlm.nih.gov/articles/PMC9339523/

This paper’s **Supplemental Table S4** contains all canonical protein sequences, mapped structural features, linear motifs, MORFs, PTMs, NLS/NES, LCS regions, and pathogenic mutations used in the NMDesc analysis.

---

## ✔ Breakdown of Table S4 Sections Used in This Viewer

### **A. Human Protein Sequences**  
Used for:
- protein backbone length  
- ID mapping  
- amino acid coordinate system  

### **B. Mapped Protein Features**  
Integrated from:
- UniProt protein features  
- InterPro domains  
- ELM SLiMs  
- MFIB MORFs  
- PhosphoSitePlus PTMs  
- NLSdb NLS/NES sequences  

### **G. LCS Mapping Across the Proteome**  
Used for:
- low complexity sequence track (green blocks)

### **H. Pathogenic Mutations Affecting Condensate-Promoting Features**  
Used optionally for:
- variant overlays when loaded by the user  

---

## ✔ Summary Table

| Track | Table S4 Section | Database Source |
|-------|-------------------|-----------------|
| Backbone | A | UniProt |
| Domains | B | InterPro |
| Protein Features | B | UniProt |
| SLiMs | B | ELM |
| MORFs | B | MFIB |
| PTMs | B | PhosphoSitePlus |
| NLS/NES | B | NLSdb |
| LCS | G | LCS mapping (Banani et al.) |
| Mutations | C/D/H | Provided in Table S4 |

---

# 🌐 Hosting

GitHub Pages configuration:
- **Branch:** `main`
- **Folder:** `docs/`

---

# 📥 Updating the Viewer

```
git add docs/
git commit -m "Update viewer"
git push
```

---

# 📜 License
MIT License.

---

# 👥 Contact

**Jake Schmidt**  
UTHealth Houston — Coban Akdemir Lab  
GitHub: schmidtjacob46

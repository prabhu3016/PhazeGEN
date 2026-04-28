# PhazeGEN 🧬

**AI-powered genome-driven platform for antimicrobial resistance analysis.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-phaze--gen--dun.vercel.app-success?style=for-the-badge)](https://phaze-gen-dun.vercel.app)

PhazeGEN is an advanced, full-stack bioinformatics platform designed to analyze pathogen genomes, predict antimicrobial resistance (AMR), and simulate clinical trial scenarios. By combining a robust Python-based machine learning engine with a highly interactive React/TypeScript frontend, PhazeGEN provides researchers with deep genomic insights, 3D protein visualizations, and an integrated AI research assistant.

---

## ✨ Key Features

* **Antimicrobial Risk ML Engine:** Utilizes pre-trained Random Forest models (`pathogen_risk_rf.pkl`) to analyze genomic sequences, extract features (ORF finding, motif scanning), and predict virulence and resistance risks.
* **Interactive Genomic Dashboards:** Dynamic UI featuring custom genome and resistance heatmaps, built with Recharts for precise data visualization.
* **Protein 3D Viewer:** Built-in structural visualization tools to analyze protein folding and mutations.
* **AI Research Assistant:** Integrated with Google Generative AI to provide contextual insights, interpret genomic data, and assist in clinical report generation.
* **Clinical Trial Simulator:** Scenario modeling tools and automated clinical report generation for therapeutic research.

## 🛠️ Tech Stack

### Frontend (Client)
* **Framework:** React 18, Vite, TypeScript
* **Styling & UI:** Custom CSS, Recharts (Data Visualization)
* **Deployment:** Vercel

### Backend (Machine Learning & API)
* **Language:** Python 3
* **AI & ML:** Scikit-Learn, Google Generative AI API
* **Pipeline:** Feature extraction (`orf_finder`, `motif_scanner`) and Risk Simulation models.

---

## 📁 System Architecture

```text
PhazeGEN/
├── backend/                       # Python Machine Learning API
│   ├── ml_engine/                 # ML Models & Feature Extraction
│   │   ├── feature_extraction/    # Sequence parsing & motif scanning
│   │   ├── models/                # Resistance, virulence, and risk models
│   │   └── pipeline/              # Main execution pipeline
│   ├── services/                  # AI Chat and external API services
│   ├── app.py                     # Backend server entry point
│   ├── bacteria_train_data.csv    # Training dataset
│   └── requirements.txt           # Python dependencies
│
└── frontend/                      # React + TypeScript UI
    ├── src/
    │   ├── components/            # UI Modules
    │   │   ├── clinical/          # Trial simulation & reporting
    │   │   ├── genomics/          # CRISPR & HGT risk panels
    │   │   ├── heatmaps/          # Recharts visualizations
    │   │   └── ChatAssistant/     # AI Assistant interface
    │   ├── Protein3DViewer.tsx    # Structural rendering
    │   └── main.tsx               # Application entry point
    ├── package.json               # Node dependencies
    └── vite.config.ts             # Vite bundler config

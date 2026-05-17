AURKB-Inhibitor-Discovery-ML-Framework
Overview
This repository hosts the complete computational framework for the identification of high-affinity Aurora Kinase B (AURKB) inhibitors. Our study integrates systematic data curation, multi-modal machine learning (Classical QSAR and Graph Convolutional Neural Networks), and structure-based validation.

Unique to this pipeline is a dual-layer regulatory approach, combining small-molecule protein inhibition with miRNA-mediated gene silencing analysis to propose a synergistic therapeutic strategy against AURKB-overexpressing malignancies.
Key Features
Multi-Modal Modeling: Combines expert-engineered 2D descriptors (XGBoost/RF) with deep learning graph representations (GCN).

Strict Applicability Domain (AD): Leverages Williams plot analysis to ensure high-confidence virtual screening results.

SAR Interpretation: Utilizes SHAP (SHapley Additive exPlanations) for mechanistic insights into structurally-driven activity.

Integrated miRNA Analysis: Cross-validated target prediction of microRNA regulators of the AURKB 3' UTR.

Structure-Based Validation: Molecular docking protocols (AutoDock Vina) targeting the 4AF3 ATP-binding pocket.

Repository Structure
├── Notebooks/
│   ├── 01_AURKB_Data_Curation_and_AD_Analysis.ipynb         # Data cleaning & AD filtering
│   ├── 02_AURKB_Classical_ML_QSAR_Modeling.ipynb            # RF, XGBoost & Validation
│   └── 03_AURKB_GCN_Consensus_and_SAR_Interpretation.ipynb  # DeepChem, SHAP & ADMET
├── Data/
│   ├── curated_training_data.csv                            # Final labeled bioactivity set
│   └── Final_Leads_Ready_for_Docking.csv                    # Top prioritized unique candidates
├── Models/
│   ├── best_qsar_model.pkl                                  # Serialized XGBoost/RF weights
│   └── gcn_checkpoint.h5                                    # DeepChem GCN model state
├── Figures/
│   ├── 06_shap_summary_plot.png                             # SAR driver interpretation
│   └── 07_admet_qed_plot.png                                # Lead drug-likeness profile
├── requirements.txt                                         # Python dependency manifest
└── README.md                                                # Project documentation
Installation & Environment Setup
To ensure reproducibility, we recommend using a Conda environment or Google Colab.

1. Clone the repository:
git clone https://github.com/prottoy47-hub/AURKB-Inhibitor-Discovery-ML-Framework.git
cd AURKB-Inhibitor-Discovery-ML-Framework
Install dependencies:
pip install -r requirements.txt
Core dependencies include: RDKit, DeepChem, Scikit-learn, XGBoost, SHAP, and Meeko.

Usage
Each notebook is designed to be self-contained but follows a sequential order. For best results, execute the notebooks in the numerical order provided in the /Notebooks directory. All paths are configured to be compatible with Google Drive integration if executed in Colab.

Citation
If you use this framework or the identified lead candidates in your research, please cite our work as follows:
License
This project is licensed under the MIT License - see the LICENSE file for details.

Contact
Fahad Fardin
Department of Pharmacy
Jahangirnagar University
Savar,Dhaka 1342


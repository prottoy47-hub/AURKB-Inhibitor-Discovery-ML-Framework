🧬 OverviewThis repository hosts a state-of-the-art computational framework for the identification of high-affinity Aurora Kinase B (AURKB) inhibitors. AURKB is a critical regulator of mitosis, and its overexpression is a hallmark of various oncogenic pathways.This pipeline introduces a dual-layer regulatory approach:Small-Molecule Inhibition: Multi-modal ML screening for $pIC_{50}$ prediction.miRNA Regulation: Integrated analysis of miRNA-mediated gene silencing targeting the AURKB 3' UTR.
🚀 Key Features
Multi-Modal Architecture: Merges expert-engineered 2D descriptors (XGBoost/Random Forest) with deep learning Graph Convolutional Networks (GCN) via DeepChem.

Rigorous Reliability: Implements a strict Applicability Domain (AD) filter using Williams plots to eliminate "black-box" predictions.

Mechanistic Explainability: Leverages SHAP (SHapley Additive exPlanations) to interpret Structure-Activity Relationships (SAR).

Structure-Based Validation: Final leads are validated through molecular docking (AutoDock Vina) targeting the ATP-binding pocket of the 4AF3 crystal structure.

📊 Performance Highlights
To be filled with your specific model results for the manuscript:

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
fahad.stu20171@juniv.edu
Department of Pharmacy
Jahangirnagar University
Savar,Dhaka 1342


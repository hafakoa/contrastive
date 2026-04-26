<<<<<<< HEAD
# contrastive
Contrastive Representation Learning for Voice-Based Autistic Trait Identification
=======
\# Contrastive Learning for Voice-Based ASD Detection



Official implementation of:



\*\*"Contrastive Representation Learning for Voice-Based Autistic Trait Identification"\*\*



\---



\## 📌 Overview



This repository provides a deep learning framework for detecting autistic traits from vocal signals using contrastive learning.



The approach leverages:

\- Time-domain and frequency-domain representations

\- Data augmentation for robust feature learning

\- Transformer-based encoders



\---



\## 🧠 Key Features



\- Multimodal contrastive learning (time + frequency)

\- Robust to heterogeneous datasets (Dutch + ReCANVo)

\- Works on verbal and non-verbal vocalizations



\---



\## 🏗️ Project Structure

src/

models/ # TFC model and classifier

datasets/ # Data loading pipeline

augmentation/ # Data augmentation

training/ # Training scripts

evaluation/ # Testing and metrics



data/ # Dataset instructions

scripts/ # Run scripts

configs/ # Config files



\---



\## ⚙️ Installation



\### Using pip



```bash

pip install -r requirements.txt

Using conda

conda env create -f environment.yml

conda activate tfc-asd

📊 Dataset



Datasets are not included due to privacy restrictions.



Used datasets:



ReCANVo (real-world vocalizations)

TalkBank (Dutch)

data/README.md

🏋️ Training

python src/training/train.py --config configs/config.yaml

🧪 Evaluation

python src/evaluation/test.py

🔁 Reproducibility

bash scripts/reproduce.sh

📈 Results

| Dataset                 | Accuracy | F1-score |

| ----------------------- | -------- | -------- |

| Mixed (Dutch + ReCANVo) | 100%\*    | 100%     |

\* Note: Based on small sample size (n=18), see paper for confidence intervals.

📎 Citation

@article{yourpaper2025,

&#x20; title={Contrastive Representation Learning for Voice-Based Autistic Trait Identification},

&#x20; author={Hajarimino Rakotomanana, Ghazal Rouhafzay},

&#x20; journal={Machine Learning and Knowledge Extraction},

&#x20; year={2025}

}

⚠️ Disclaimer

This tool is for research purposes only and is not intended for clinical diagnosis.

🙏 Acknowledgements

Inspired by contrastive learning frameworks such as SupContrast, TF-C.



\---



\# 📦 `requirements.txt`



```txt

torch

numpy

scikit-learn

matplotlib

scipy

tqdm



>>>>>>> fb7ed0e (Initial push)

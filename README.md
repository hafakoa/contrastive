# Contrastive Representation Learning for Voice-Based Autistic Trait Identification
#### Authors: Hajarimino Rakotomanana (rhajarimino@gmail.com), Ghazal Rouhafzay (ghazal.rouhafzay@umoncton.ca), <br/>

#### Paper: [Preprint](https://doi.org/10.20944/preprints202604.1071.v1)

## 📌 Overview 

Official implementation of :

\*\*"Contrastive Representation Learning for Voice-Based Autistic Trait Identification"\*\*

This repository provides a deep learning framework for detecting autistic traits from vocal signals using contrastive learning.



The approach leverages:

\- Time-domain and frequency-domain representations of [Xiang et al.](https://zitniklab.hms.harvard.edu/projects/TF-C/)

\- Data augmentation for robust feature learning

\- Transformer-based encoders

\- Supervised Contrastive Learning of [Prannay et al.](https://arxiv.org/abs/2004.11362)


Specifically, we leverage the complementary nature of temporal and spectral voice representations to enforce cross-view consistency while explicitly incorporating diagnostic labels during training.

The proposed objective is designed to identify traits associated with Autism Spectrum Disorder (ASD) by simultaneously minimizing intra-class variability and maximizing inter-class separability in the learned embedding space. By integrating label-informed contrastive constraints, the model promotes more discriminative representations and improves robustness to inter-speaker variability, thereby enhancing generalization to previously unseen individuals.

<p align="center">
    <img src="images/ASD_pipeline_v3.png" width="750" align="center">
</p>

The figure above provides an overview of the proposed pipeline. The architecture consists of three main stages: (i) time–frequency feature extraction and dual-branch encoding, (ii) supervised contrastive representation learning, and (iii) downstream fine-tuning with a lightweight classification head. The figure illustrates how temporal and spectral representations are jointly optimized under contrastive supervision before being transferred to the diagnostic classification task.

## 🧠 Key Features



\- Multimodal contrastive learning (time + frequency)

\- Robust to heterogeneous datasets (Dutch + ReCANVo)

\- Works on verbal and non-verbal vocalizations



\---



## 🏗️ Project Structure

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



## ⚙️ Installation



### Using pip



```bash

pip install -r requirements.txt

Using conda

conda env create -f environment.yml

conda activate tfc-asd
```

## 📊 Dataset



Datasets are not included due to privacy restrictions.



Used datasets:



ReCANVo (real-world vocalizations)

TalkBank (Dutch)

data/README.md

## 🏋️ Training

python src/training/train.py --config configs/config.yaml

## 🧪 Evaluation

python src/evaluation/test.py

## 🔁 Reproducibility

bash scripts/reproduce.sh

## 📈 Results

| Dataset                 | Accuracy | F1-score |

| ----------------------- | -------- | -------- |

| Mixed (Dutch + ReCANVo) | 100%\*    | 100%     |

\* Note: Based on small sample size (n=18), see paper for confidence intervals.

## 📎 Citation

@article{yourpaper2025,

&#x20; title={Contrastive Representation Learning for Voice-Based Autistic Trait Identification},

&#x20; author={Hajarimino Rakotomanana, Ghazal Rouhafzay},

&#x20; journal={Machine Learning and Knowledge Extraction},

&#x20; year={2025}

}

## ⚠️ Disclaimer

This tool is for research purposes only and is not intended for clinical diagnosis.

## 🙏 License & Acknowledgements

Inspired by contrastive learning frameworks such as SupContrast, TF-C.

This project incorporates code from [TF-C Pretraining](https://github.com/mims-harvard/TFC-pretraining) by the Zitnik Lab at Harvard, which is licensed under the MIT License.

### Original Copyright Notice:
Copyright (c) 2022 Machine Learning for Medicine and Science @ Harvard

A copy of the full MIT License text is included in the [LICENSE](./LICENSE) file of this repository.


\---



## 📦 `requirements.txt`

The full requirements.txt are included in the [requirements.txt](./requirements.txt) file of this repository.

```txt

torch

librosa

huggingface_hub

transformers

scikit-learn

matplotlib

scipy

tqdm

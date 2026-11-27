# Notebooks d'entraînement Kouman AI (CPT, SFT et Quantification GGUF)

Ce dossier regroupe les notebooks complets utilisés pour pré-entraîner (CPT), aligner (SFT) et quantifier les modèles trilingues français / baoulé / dioula de Tree AI Lab.

## 1. Kouman 1.0 (`Gemma 2 2B`)

Dossier : `kouman-1.0/`

| Étape | Notebook | Description |
| :--- | :--- | :--- |
| 1 | `01_cpt_pretokenisation_shards_gemma2_2b.ipynb` | Pré-tokénisation et génération des shards 2048 tokens |
| 2 | `02_cpt_entrainement_relais_gemma2_2b_rocm.ipynb` | Entraînement CPT par sessions relais sur GPU AMD ROCm |
| 3 | `03_sft_dataset_kouman_1_0.ipynb` | Construction et audit du jeu de données SFT propre |
| 4 | `04_sft_entrainement_kouman_1_0_rocm.ipynb` | Entraînement SFT sur AMD ROCm et fusion du modèle final |

## 2. Kouman Edge 1B (`Llama 3.2 1B`)

Dossier : `kouman-edge-1b/`

| Étape | Notebook | Description |
| :--- | :--- | :--- |
| 1 | `01_cpt_pretokenisation_shards_llama32_1b.ipynb` | Pré-tokénisation et génération des shards 2048 tokens |
| 2 | `02_cpt_entrainement_relais_llama32_1b_rocm.ipynb` | Entraînement CPT par sessions relais sur GPU AMD ROCm (`Llama 3.2 1B`) |
| 3 | `03_sft_v5_kouman_edge_1b_rocm_colab.ipynb` | Entraînement SFT V5 (documents entiers, format conversationnel, LoRA FP32) et export |
| 4 | `04_quantification_gguf_kouman_edge_1b.ipynb` | Quantification GGUF complète (`Q8_0` à `Q2_K`) avec calibration `imatrix` 4 langues (`llama.cpp`) |

# AraFinNews: The Arabic Financial News Dataset (212K)

**AraFinNews** is the largest openly available dataset of Arabic financial news, comprising **212,000 full-length articles** collected from [Argaam.com](https://www.argaam.com/) — a leading financial news portal in the Arab world.  
The dataset provides structured, machine-readable text suitable for research in **financial NLP**, **abstractive summarisation**, **event extraction**, and **domain-specific language modelling**.

Comparable to the **CNN/DailyMail** dataset for English, AraFinNews offers an Arabic equivalent for headline-style abstractive summarisation. Each record pairs a full Arabic financial article with its professionally written headline, enabling high-quality training and evaluation of summarisation and financial text understanding systems.

---

## 📰 Dataset Overview

| Field   | Description                                   |
|---------|-----------------------------------------------|
| `id`    | Unique numeric identifier                     |
| `title` | Arabic headline (financial news title)        |
| `date`  | Publication date (ISO format)                 |
| `article` | Full article text                           |
| `url`   | Public link on *Argaam.com*                   |

- **Total articles:** 212,000  
- **Language:** Modern Standard Arabic  
- **Domain:** Finance, markets, economics, corporate activity  
- **Format:** CSV (UTF-8)  
- **Licence:** CC BY-NC 4.0  

---

## ⚙️ Updated Data Splits

In addition to the original ID lists, the repository now includes **fully populated split files**:

- `train.csv` — 80% of the dataset  
- `validation.csv` — 10%  
- `test.csv` — 10%

These files contain **the complete article and headline rows**, making them directly compatible with the Hugging Face Dataset Viewer and eliminating the need to reconstruct splits manually.

The older ID-only files are still included for reference:

- `AraFinNews_train_ids.csv`  
- `AraFinNews_val_ids.csv`  
- `AraFinNews_test_ids.csv`

These can be used if a user prefers to work from the master file `AraFinNews.csv`.

---

## ⚙️ Intended Use

AraFinNews supports research in:

- Abstractive and extractive summarisation  
- Financial event and entity extraction  
- Sentiment and stance analysis in financial narratives  
- Domain-specific pretraining and adaptation of Arabic LLMs  
- Financial question answering and narrative analysis  

The dataset is released strictly for **non-commercial research and educational use**.

---

## 📦 Access and Usage

### Load the full dataset

    import pandas as pd

    df = pd.read_csv("AraFinNews.csv")
    df.sample(5)

### Load directly from the full splits

    import pandas as pd

    train = pd.read_csv("train.csv")
    val = pd.read_csv("validation.csv")
    test = pd.read_csv("test.csv")

### (Legacy) Load splits using ID files

    import pandas as pd

    df = pd.read_csv("AraFinNews.csv")
    train_ids = pd.read_csv("AraFinNews_train_ids.csv")["id"]
    train_df = df[df["id"].isin(train_ids)]

---

## 📚 Citation

If you use this dataset, please cite:

> **El-Haj, M.** & **Rayson, P.** (2025). *AraFinNews: Arabic Financial Summarisation with Domain-Adapted LLMs.* Proceedings of IEEE Big Data 2025.

This work is associated with the following preprint:  
**https://arxiv.org/abs/2511.01265**

---

## 🏛️ Repository Structure

    AraFinNews/
    │
    ├── AraFinNews.csv
    ├── train.csv
    ├── validation.csv
    ├── test.csv
    │
    ├── AraFinNews_train_ids.csv
    ├── AraFinNews_val_ids.csv
    ├── AraFinNews_test_ids.csv
    │
    ├── AraFinNews_json_files/
    │   ├── 000001.json
    │   ├── 000002.json
    │   └── ...
    │
    └── README.md

---

**Contact:**  
Mo El-Haj  
VinUniversity, Hanoi / Lancaster University, UK  
dr.melhaj@gmail.com
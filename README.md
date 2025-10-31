# AraFinNews: The Arabic Financial News Dataset (212K)

**AraFinNews** is the largest open dataset of Arabic financial news, containing **212,000 full-length articles** collected from [Argaam.com](https://www.argaam.com/) — one of the most reputable financial media outlets in the Arab world.  
The dataset provides structured, machine-readable text and metadata for use in research on **Arabic financial language**, **abstractive summarisation**, **event extraction**, and **domain-specific language modelling**.

Comparable in purpose to the well-known **CNN/DailyMail** datasets for English, AraFinNews offers an Arabic equivalent for large-scale, headline-style summarisation. Each record pairs a full Arabic financial article with its professionally written headline, making it ideal for developing and evaluating models that require concise, factual, and stylistically coherent summaries.
---

## 📰 Dataset Overview

| Field | Description |
|--------|-------------|
| `id` | Unique numeric identifier for each article |
| `title` | Headline in Arabic (financial news title) |
| `date` | Publication date in ISO format |
| `article` | Full body text of the financial news article |
| `url` | Original public link on *Argaam.com* |

- **Total records:** 212,000  
- **Language:** Modern Standard Arabic (MSA)  
- **Domain:** Finance, economics, markets, and corporate announcements  
- **Format:** CSV (`AraFinNews.csv`) encoded in UTF-8  
- **Licence:** CC BY-NC 4.0 (Attribution–NonCommercial)

---

## ⚙️ Intended Use

The **AraFinNews** dataset is designed to advance research in:

- Arabic **abstractive and extractive summarisation**  
- **Financial event and entity extraction**  
- **Sentiment and stance analysis in financial contexts**  
- **Named entity recognition** (companies, currencies, indices)  
- **Domain-specific LLM pretraining** and financial language modelling  

The dataset is released **strictly for non-commercial research and educational purposes**.  
Redistribution of raw content or automated scraping of linked sources is **not permitted**.

---

## 📦 Access and Usage

You can load the dataset directly in Python:

```python
import pandas as pd
df = pd.read_csv("AraFinNews.csv")
print(df.sample(5))

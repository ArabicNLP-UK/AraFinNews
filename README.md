# Argaam-FinNews: Arabic Financial News Dataset (60K)

**Argaam-FinNews** is a large-scale dataset of **60,000 Arabic financial news articles** collected from [Argaam.com](https://www.argaam.com/), one of the leading financial media platforms in the Gulf region.  
The dataset provides **structured metadata** — including article IDs, titles, publication dates, full article text, and original URLs — enabling research on Arabic financial language, summarisation, information extraction, and domain-specific language modelling.

---

## 📰 Dataset Overview

| Field | Description |
|--------|--------------|
| `id` | Unique numeric identifier for each article |
| `title` | Article headline in Arabic |
| `date` | Publication date (ISO format) |
| `article` | Full body text of the financial news item |
| `url` | Original source link from *Argaam.com* |

- **Total records:** 60,000  
- **Language:** Modern Standard Arabic (MSA)  
- **Domain:** Finance, economics, markets, and corporate disclosures  
- **Format:** CSV (`argaam_finnews.csv`) encoded in UTF-8  
- **Licence:** CC BY-NC 4.0 (Attribution–NonCommercial)

---

## ⚙️ Intended Use

This dataset supports research in:

- Arabic **abstractive summarisation**
- **Financial event extraction**
- **Sentiment and stance analysis**
- **Named entity recognition (companies, currencies, indices)**
- **Domain adaptation and financial LLM pretraining**

The dataset is released **for research and educational use only**.  
Commercial redistribution or automated scraping of linked content is **not permitted**.

---

## 📦 Access and Usage

You can load the dataset directly from the CSV file:

```python
import pandas as pd
df = pd.read_csv("argaam_finnews.csv")
print(df.head())

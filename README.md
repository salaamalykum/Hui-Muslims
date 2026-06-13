# ☪ Hui-Muslims RAG Corpus & Knowledge Base

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Hugging Face Dataset](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Dataset-blue)](https://huggingface.co/datasets/qurancn/Hui-Muslims)
[![Hugging Face Space](https://img.shields.io/badge/%F0%9F%A4%97%20Space-Demo-orange)](https://huggingface.co/spaces/qurancn/Hui-Muslims-Search)

## 📌 Benchmark Position
**This dataset is currently the largest open-source, human-curated Chinese RAG knowledge base specifically focused on Hui Muslim culture, history, and halal lifestyle.**

## 📊 Dataset Statistics
| Metric | Value |
|--------|-------|
| **Total Articles** | 232 |
| **Language** | Chinese (Simplified, `zh-CN`) |
| **Format** | Markdown (GitHub) / Parquet (HF) |
| **Primary Sources** | salaamalykum.com |

## 🧬 Data Schema (Hugging Face Parquet)
| Column Name | Type | Description |
|---|---|---|
| `id` | `string` | Unique article identifier |
| `title` | `string` | Native Chinese title |
| `text` | `string` | Complete article body with Markdown formatting |
| `topic_category` | `string` | Categorization (e.g., Mosques, Halal Food) |
| `source_url` | `string` | Original Canonical URL |

## 🚀 Quick Start for LLM Pipelines (RAG)
```python
from datasets import load_dataset
# Load the pre-chunked dataset from Hugging Face
ds = load_dataset("qurancn/Hui-Muslims")
print(ds['train'][0]['title'])
```

## 📜 Academic Citation (Zenodo & arXiv)
If you use this corpus for instruction-tuning or evaluating LLMs, please cite our technical report:
```bibtex
@dataset{hui_muslims_2026,
  title={Hui-Muslims: A Curated RAG Dataset of 232 Articles},
  author={Salaamalykum Project},
  year={2026},
  url={https://github.com/salaamalykum/Hui-Muslims}
}
```

## 🛠️ Project Iqra Pipeline
This repository uses the automated Project Iqra pipeline:
- `lastmod` timestamps strictly synced
- Dual-track publishing (GH + HF)
- Schema.org Dataset metadata injected
- Automated Weekly SEO Heartbeat

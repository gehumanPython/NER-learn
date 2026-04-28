# Learn Named Entity Recognition (NER)

A hands-on tutorial series to learn NER from scratch — from rule-based approaches to fine-tuning transformer models.

## What is NER?

**Named Entity Recognition (NER)** is an NLP task that identifies and classifies named entities in text into predefined categories such as **Person**, **Organization**, **Location**, **Date**, **Money**, etc.

```
Input:  "Apple was founded by Steve Jobs in Cupertino in 1976."
Output: [Apple → ORG] [Steve Jobs → PERSON] [Cupertino → GPE] [1976 → DATE]
```

## Learning Path

| # | Notebook | Topics | Level |
|---|----------|--------|-------|
| 1 | [01_ner_fundamentals.ipynb](notebooks/01_ner_fundamentals.ipynb) | What is NER, spaCy basics, entity types, visualizing entities | Beginner |
| 2 | [02_custom_ner_spacy.ipynb](notebooks/02_custom_ner_spacy.ipynb) | Training custom NER models with spaCy, data formatting, evaluation | Intermediate |
| 3 | [03_ner_with_transformers.ipynb](notebooks/03_ner_with_transformers.ipynb) | BERT for NER, Hugging Face pipeline, fine-tuning on CoNLL-2003 | Advanced |

## Quick Start

```bash
# Clone the repo
git clone https://github.com/<your-username>/learn-ner.git
cd learn-ner

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Download spaCy model
python -m spacy download en_core_web_sm

# Launch Jupyter
jupyter notebook
```

## Key Concepts Covered

- **IOB/BIO Tagging** — How NER labels are encoded (B-PER, I-PER, O)
- **Rule-based NER** — Using patterns and gazetteers
- **Statistical NER** — spaCy's transition-based NER
- **Transformer NER** — Fine-tuning BERT for token classification
- **Evaluation Metrics** — Precision, Recall, F1 per entity type
- **Data Formats** — CoNLL, spaCy DocBin, Hugging Face datasets

## Entity Types Reference

| Tag | Meaning | Example |
|-----|---------|---------|
| PERSON | People | *Steve Jobs* |
| ORG | Organizations | *Apple Inc.* |
| GPE | Countries, cities, states | *California* |
| DATE | Dates and periods | *January 2024* |
| MONEY | Monetary values | *$500 million* |
| LOC | Non-GPE locations | *Mount Everest* |
| PRODUCT | Objects, vehicles, foods | *iPhone 15* |
| EVENT | Named events | *World Cup* |

## Project Structure

```
learn-ner/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   ├── 01_ner_fundamentals.ipynb
│   ├── 02_custom_ner_spacy.ipynb
│   └── 03_ner_with_transformers.ipynb
└── data/
    └── sample_train.json
```

## Requirements

- Python 3.8+
- See [requirements.txt](requirements.txt) for full list

## License

MIT

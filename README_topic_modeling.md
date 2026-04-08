# Topic Modeling with LDA & LSI 📚
### Discovering Hidden Topics in Text using Latent Dirichlet Allocation

An unsupervised NLP project that extracts abstract topics from a large collection of Kaggle dataset descriptions using **LDA** and **LSI** topic models, with interactive **pyLDAvis** visualization.

---

## Overview

Topic modeling is a powerful unsupervised technique to discover hidden thematic structures in large text corpora — used widely in social media analysis, news categorization, and document clustering.

This project applies **Latent Dirichlet Allocation (LDA)** — originally proposed by David Blei et al. (2003) — and **Latent Semantic Indexing (LSI)** to a real-world dataset of Kaggle dataset descriptions, uncovering 15 distinct topics with interactive visualization.

---

## How it works

```
Raw Text → Preprocessing → Dictionary → Bag-of-Words Corpus
→ LDA Model (15 topics) → Topic Visualization (pyLDAvis)
```

1. **Load dataset** — Kaggle dataset descriptions (loaded directly from public URL)
2. **Preprocessing pipeline:**
   - Tokenization with RegexpTokenizer
   - Stopword removal (NLTK English stopwords)
   - Lemmatization (WordNetLemmatizer)
   - Single-character word removal
3. **Dictionary creation** — Gensim Dictionary with frequency filtering
4. **Corpus** — Bag-of-Words document-term matrix
5. **LDA training** — 15 topics, 10 passes, alpha='auto'
6. **LSI model** — Alternative topic model for comparison
7. **Visualization** — Interactive pyLDAvis topic explorer

---

## Sample output

```
=== 15 Topics with Top Words ===

Topic #0:  data + analysis + machine + learning + prediction
Topic #1:  image + classification + deep + neural + network
Topic #2:  sales + price + market + customer + revenue
Topic #3:  health + disease + medical + patient + clinical
Topic #4:  text + nlp + sentiment + language + review
...
```

---

## Interactive visualization

The project generates an interactive **pyLDAvis** dashboard saved as `topic_model_visualization.html` — showing topic clusters, term relevance, and inter-topic distances in a 2D space.

---

## Tech stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Gensim (LdaModel) | LDA topic model training |
| Gensim (LsiModel) | LSI topic model training |
| Gensim (Dictionary, corpora) | Vocabulary & corpus management |
| NLTK | Tokenization, stopwords, lemmatization |
| pyLDAvis | Interactive topic visualization |
| Pandas | Dataset loading and exploration |

---

## How to run

```bash
# Install dependencies
pip install gensim nltk pyLDAvis pandas

# Download NLTK data
python -c "import nltk; nltk.download('stopwords'); nltk.download('wordnet')"

# Run the notebook
jupyter notebook Topic_Modeling.ipynb
```

> Dataset loads automatically from public URL — no local file needed.

---

## Model details

| Parameter | Value |
|-----------|-------|
| Algorithm | Latent Dirichlet Allocation (LDA) |
| Number of topics | 15 |
| Training passes | 10 |
| Chunk size | 100 |
| Alpha | auto |
| Random state | 42 |
| Frequency filter | min 2 docs, max 50% of docs |

---

## Key concepts demonstrated

- **Unsupervised learning** — discovering structure with no labeled data
- **Text preprocessing pipeline** — tokenization, stopword removal, lemmatization
- **Bag-of-Words** — converting documents to numerical corpus
- **LDA** — probabilistic topic model assigning word distributions to topics
- **LSI** — dimensionality reduction approach to topic extraction
- **pyLDAvis** — interactive visualization of topic-term relationships

---

## Dataset

- **Source:** [Kaggle Datasets CSV](https://raw.githubusercontent.com/subashgandyer/datasets/main/kaggledatasets.csv)
- **Feature used:** `Description` column
- **Size:** Multiple dataset descriptions from Kaggle

---

## Author

**Atageldi Kakabayev** — AI/ML Developer | GenAI · NLP · Topic Modeling  
[LinkedIn](https://linkedin.com/in/atageldi-kakabayev) · [GitHub](https://github.com/Atash22)

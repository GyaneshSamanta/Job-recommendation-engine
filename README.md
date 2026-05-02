# Job Recommendation Engine

> **Helping students choose where their career compass points next — one similarity score at a time.**

![Status](https://img.shields.io/badge/status-research--prototype-blue)
![Python](https://img.shields.io/badge/python-3.8+-yellow)
![Notebook](https://img.shields.io/badge/jupyter-notebook-orange)

---

## About

A research notebook built for **iSchoolConnect** that recommends jobs to students considering higher studies abroad. It answers two questions:

- **Who?** Students applying to foreign universities and trying to map degrees to careers.
- **What?** A content-based job recommender powered by a Kaggle job-postings dataset.
- **Where?** A standalone Jupyter notebook — no server, no UI, just reproducible analysis.
- **When?** Built in 2022 as part of an ML research engagement.
- **Why?** Most students pick a degree without knowing what jobs it actually unlocks. This makes the link explicit.

## The Story

We started with a Kaggle dump of job postings and a simple hypothesis: students don't need a job board, they need a *map*. The notebook walks through that map in two passes.

The **first pass** is a "more like this" engine — feed it a job title, get back the postings that demand a similar skill stack. The **second pass** flips the question: feed in your education, qualifications, and experience, and get a ranked list of roles that people with similar profiles have landed.

The honest finding: the recommender shines on tech roles (CS, dev, IT) where the dataset is dense, and stumbles on long-tail roles (accounting, trades, non-IT services) where the postings are sparse. That gap is the next chapter.

## Gallery

> Open `noob_job_recommendation.ipynb` to see the full walkthrough — EDA, feature engineering, similarity matrices, and recommendation outputs.

---

## Tech Stack

| Layer | Tools |
|------|-------|
| Language | Python 3 |
| Environment | Jupyter Notebook |
| Data | Kaggle job-postings dataset |
| ML | scikit-learn, pandas, numpy (TF-IDF + cosine similarity) |
| Versioning | Git, GitHub |

## Repo Structure

```
Job-recommendation-engine/
├── noob_job_recommendation.ipynb   # Main notebook (EDA + model + recs)
├── dataset.txt                     # Pointer to Kaggle dataset
└── README.md
```

## Getting Started

```bash
git clone https://github.com/GyaneshSamanta/Job-recommendation-engine.git
cd Job-recommendation-engine

# Recommended: a fresh venv
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install jupyter pandas numpy scikit-learn

# Grab the Kaggle dataset referenced in dataset.txt, then:
jupyter notebook noob_job_recommendation.ipynb
```

## Contributing

This is a research artifact, not a maintained library — but PRs that improve the non-IT coverage, swap TF-IDF for embeddings, or wrap the model in an API are welcome.

## License

No license file present — treat as **all rights reserved** until one is added. Reach out before reusing.

## Credits

- **Gyanesh Samanta** — research, modelling, notebook authoring
- **iSchoolConnect** — research sponsor and problem owner
- **Kaggle community** — for the open job-postings dataset that made this possible

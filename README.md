# Multihead Text Mining from COVID-19 Feedback Using Machine Learning, Deep Learning, and Hybrid Deep Learning Approaches

Published research on Bengali text classification, analyzing the impact of COVID-19 on students' academic, mental, and social well-being using 8 classical ML algorithms, 3 deep learning architectures, and 2 hybrid DL models.

**Published in:** *Journal of Sensors*, Wiley, Volume 2024, Article ID 3027199 (27 pages)
**DOI:** [10.1155/2024/3027199](https://doi.org/10.1155/2024/3027199)
**Authors:** Khadijatul Kobra, **Samrina Sarkar Sammi**, Naimur Rahman, Sharun Akter Khushbu, Mirajul Islam
**Affiliation:** Department of Computer Science and Engineering, Daffodil International University, Dhaka, Bangladesh
**License:** Open access, Creative Commons Attribution License

---

## Abstract

This study examines the impact of the COVID-19 epidemic on students in Bangladesh through text classification using various machine learning (ML) algorithms and deep learning (DL) models. The pandemic led to emergency crisis protocols in the country, including self-quarantine and the closure of educational and governmental institutions, resulting in significant negative impacts on individuals' physical and mental health. To better understand the psychological effects of the epidemic, we collected survey data from 400 students across various divisions of Bangladesh using self-administered questionnaires. The study deployed eight ML algorithms and DL models, including LSTM, BiLSTM, and CNN, to classify the effects on students' academic, mental, and social lives, achieving accuracies of up to 98.75%.

## Novelty

To the best of our knowledge, this is the first study on multi-head text mining for Bengali COVID-19 impact-related data — classifying the same survey response across three distinct life-impact dimensions (academic, mental health, social) rather than a single sentiment label.

## Dataset

- **Collection:** Self-administered questionnaires (22 different question sets) completed in person by 400 Bangladeshi students aged 10+, across schools, colleges, and universities, using stratified sampling by educational level and gender
- **Structure:** 3 free-text response columns (impact on academic life, mental health, social life) + 1 shared Positive/Negative sentiment label, annotated by multiple independent annotators with inter-annotator agreement measured via Cohen's kappa
- **Language:** Bengali (Bangla)
- **Size:** 400 rows, perfectly balanced (200 Positive / 200 Negative)

## Methodology

**Preprocessing:** Duplicate removal, short-text filtering, Bangla punctuation removal, manual Bengali stop-word removal, stemming, label encoding, tokenization (Keras Tokenizer), and sequence padding.

**Models evaluated:**
- **Classical ML (8):** Random Forest, Multinomial Naïve Bayes, Decision Tree, Logistic Regression, Linear SVM, K-Nearest Neighbor, Stochastic Gradient Descent, RBF SVM
- **Deep Learning (3):** LSTM, BiLSTM, CNN
- **Hybrid DL (2):** CNN-LSTM, CNN-BiLSTM

**Evaluation:** 80/20 train/test split for ML; 80/20 train/validation/test split for DL, trained for 10 epochs, evaluated on Accuracy, Precision, Recall, and F1 score.

## Key Results

| Input Column | Best Classical ML | Best DL Model |
|---|---|---|
| Academic Life | SGD — 95.00% accuracy | BiLSTM — 92.50% accuracy |
| Mental Health | KNN — 93.75% accuracy | LSTM — 98.75% accuracy |
| Social Life | SGD / Multi-NB — 95.00% accuracy | BiLSTM / CNN / CNN-LSTM — 92.50% accuracy |

Hybrid DL models (CNN-LSTM, CNN-BiLSTM) also produced strong, competitive scores across all three dimensions. Full precision/recall/F1 breakdowns, training curves, and loss function comparisons (MAE, MSE, RMSE, R², MSLE, RMSLE) are reported in the published paper.

## Limitations (as discussed in the paper)

- Manual, in-person data collection from a single population (Bangladeshi students) may introduce sampling bias
- Sample size (400) is small relative to typical DL training requirements — reflected in some models (CNN, CNN-LSTM) showing negative R² scores, indicating a poor fit for those specific architectures on this dataset size
- Findings are specific to the Bengali-speaking student population studied; the paper notes this methodology could be extended to other languages and populations

## Follow-Up Work

See my related project, [`covid19-bangla-text-mining-ml-dl`'s companion repo] — a follow-up study fine-tuning a pretrained transformer (BanglaBERT) on this same dataset, testing whether a modern transformer outperforms the classical ML/DL models used here.

## Citation

If referencing this work, please cite:

```
Kobra, K., Sarkar Sammi, S., Rahman, N., Khushbu, S. A., & Islam, M. (2024).
Multihead Text Mining from COVID-19 Feedback Using Machine Learning, Deep Learning,
and Hybrid Deep Learning Approaches. Journal of Sensors, 2024, Article ID 3027199.
https://doi.org/10.1155/2024/3027199
```

## Tech Stack

Python, pandas, scikit-learn, Keras/TensorFlow, NLTK-style Bengali preprocessing

```

## About Me

**Samrina Sarkar Sammi** — M2 Data Science & Network Intelligence student, Télécom SudParis

[LinkedIn](https://www.linkedin.com/in/samrina-sarkar-sammi-a8b716424/) · [GitHub](https://github.com/samrinasarkar-sammi) · samrinasarkar@gmail.com

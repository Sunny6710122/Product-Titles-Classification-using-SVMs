# Product Titles Classification using SVMs 📦📊

## Introduction 🌟

This repository contains the implementation of **Product Title Classification** using **Support Vector Machine (SVM)** models. The study explores various methods for classifying product titles into predefined categories and focuses on enhancing accuracy through different feature extraction techniques and SVM configurations.

---

## Objective 🎯

The primary goal of this project is to develop a robust machine learning model capable of accurately classifying product titles into specific categories. The implementation involves:
- Experimenting with various feature extraction methods.
- Utilizing and comparing different SVM models.
- Determining the optimal approach for accurate classification.

---

## Data Preprocessing 🔧

- **Text Normalization**: Converts product titles to lowercase for uniformity.
- **Tokenization**: Splits titles into individual words or phrases.
- **Label Encoding**: Encodes categories as integers to make them suitable for machine learning algorithms.
- **TF-IDF Vectorization**: Transforms text data into numerical vectors using TF-IDF weights. The project compares:
  - **Unigrams**: Single words.
  - **Bigrams**: Consecutive word pairs.

---

## Feature Extraction Techniques 🛠️

- **Unigrams**: Each word in the title is treated as a separate feature.
- **Bigrams**: Pairs of consecutive words capture additional context.
- **Degree-2 Polynomial Mapping (poly2)**: Expands the feature space to include squared terms and interaction terms, enhancing representation.

---

## SVM Models 🚀

- **One-vs-One (OvO)**: Constructs a binary classifier for each pair of classes, training \(\frac{n(n-1)}{2}\) classifiers.
- **One-vs-Rest (OvR)**: Constructs a binary classifier for each class against all others, training \(n\) classifiers.
- **Crammer & Singer**: Solves a single optimization problem for all classes simultaneously, offering computational efficiency and accuracy.

---

## Comparison of Methods 📈

- **Bigram Features**: Significantly improve classification performance compared to unigrams.
- **Polynomial Features (poly2)**: Show the best results, reducing classification errors to 70% of baseline.

### SVM Performance

- **OvO**: Competitive performance but computationally intensive.
- **OvR**: Similar performance with fewer classifiers.
- **Crammer & Singer**: Outperforms others in accuracy and computational efficiency.

---

## Results ✅

- **Bigram + Unigram**: Results in 11,799,345 features, improving classification accuracy.
- **Polynomial Mapping (poly2)**: Expands features to 41,689,205, yielding the best results across all SVM strategies.

### Performance Metrics
- **REbaseline**: Achieves a reduction in classification errors to approximately 70% of the baseline error.

---

## Implementation Details 🖥️

- **Normalization**: Ensures each instance has unit length to prevent dominance by any single feature.
- **Hashing Technique**: Efficiently manages the vast feature space by eliminating unused features.

---

## Conclusion 🏁

Sophisticated feature extraction techniques like bigrams and polynomial mappings significantly improve classification accuracy. Among SVM models, the **Crammer & Singer method** stands out for its superior performance and computational efficiency. This project underscores the importance of feature engineering in text classification tasks and provides insights into implementing effective SVM models for multi-class classification.

---

Explore the repository to learn more about advanced text classification using SVMs! 🚀✨

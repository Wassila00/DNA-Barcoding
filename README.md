# 🌱 Species Classification using DNA Barcoding

## 📌 Project Overview
This project aims to predict plant species based on DNA sequence data using the DNA Barcoding method. By analyzing short standardized sequences from specific gene regions (e.g., **rbcL**, **matK** ,...), we use machine learning techniques to classify species with high accuracy.

## 🧬 What is DNA Barcoding?
DNA Barcoding is a technique for identifying species using a short genetic sequence from a standardized region of the genome. Each species typically has a unique pattern in these regions, allowing for accurate classification using bioinformatics tools.

## 📂 Dataset
- **Source**: [BOLD Systems](https://www.boldsystems.org/)
- **Format**: Original file was in FASTA format, later converted to CSV (plants_cleaned_final.csv)
- **Important Columns**:
  - `Gene_Region`: Target gene region (e.g., rbcL)
  - `Class`, `Order`, `Family`, `Genus`, `Species`: Taxonomy details
  - `Sequence`: Raw DNA sequence

## 🛠️ Preprocessing
- Removal of incomplete rows
- Removal of unused columns (e.g., ID, Country, Phylum...)
- Encoding:
  - `Gene_Region` via **OneHotEncoder**
  - `Sequence` via **CountVectorizer** or **TfidfVectorizer** with k-mer analysis (k=3 to 8)
  - `Species` via **LabelEncoder**

## 🧠 Models Used
- **Random Forest** 🌳
- **Naive Bayes** 📊
- **Support Vector Machine** (SGDClassifier) ⚙️
- **XGBoost** 🚀
- **Neural Network (MLP)** 🧠
- **CNN and RNN** (with Keras) 🧬

## 📈 Evaluation
- Used metrics: **Accuracy**, **F1-score**, **Precision**, **Recall**
- **Best Result**:  
  Random Forest with CountVectorizer (k=6)  
  → Accuracy: **87%**

## 🚀 Improvements
- Hyperparameter tuning using **GridSearchCV**
- K-mer optimization
- Advanced models (CNN, RNN, XGBoost)
- Stratified K-Fold for balanced class splits

## 🧪 Prediction Example
Tested the trained model on external DNA sequences to predict the species. 

## 📎 Dependencies
- Python ≥ 3.8
- scikit-learn
- pandas
- numpy
- BioPython
- xgboost
- tensorflow / keras



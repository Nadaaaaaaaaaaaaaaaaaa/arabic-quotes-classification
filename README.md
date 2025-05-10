# arabic-quotes-classification

This project focuses on the **automatic classification of Arabic quotes** into predefined thematic categories using Natural Language Processing (NLP) techniques. Given the linguistic richness and complexity of the Arabic language, our work aims to address its specific challenges through a complete pipeline of data collection, preprocessing, and classification.

---

## 📚 Table of Contents

1. [Introduction](#introduction)  
2. [Data Collection](#data-collection)  
3. [Data Preprocessing](#data-preprocessing)  
4. [Model Training](#model-training)  
5. [Results](#results)  
6. [Challenges & Improvements](#challenges--improvements)  
7. [Technologies Used](#technologies-used)  
8. [How to Run the Project](#how-to-run-the-project)

---

## 🧠 Introduction

### Background
The diversity of Arabic dialects and writing styles poses a real challenge for text classification. This project applies NLP to automatically classify quotes in Arabic into relevant themes, such as **honesty**, **ambition**, **science**, **collaboration**, and more.

### Objectives
- Build a system to automatically classify Arabic quotes.
- Develop a complete pipeline: data collection, preprocessing, and model training.
- Analyze the performance of classification models.

---

## 📊 Data Collection

- **Method**: Web scraping  
- **Sources**: Arabic forums, blogs, social media (Twitter, Facebook), and news websites  
- **Dataset size**: 23,877 Arabic quotes  
- **Labeling**: Each quote is labeled with one of many thematic categories  
- **Class imbalance**:  
  - Majority class: 905 samples  
  - Minority class: 1 sample  
  - Gini Index: 0.9855 (high imbalance)

---

## 🔧 Data Preprocessing

The following steps were applied to clean and prepare the Arabic text:

- Removing diacritics
- Removing English words
- Removing meaningless/repetitive sentences
- Removing digits and special characters
- Tokenization
- Removing Arabic stop words
- Sampling to reduce class imbalance
- Light stemming with **Tashaphyne**
- Label encoding of categories
- TF-IDF vectorization

---

## 🧪 Model Training

- **Model used**: Decision Tree Classifier
- **Evaluation Metrics**:
  - Log Loss: 3.7824
  - Macro F1 Score: 0.5082
  - Weighted Accuracy: 0.7438

- **AUC Analysis**:
  - 92 classes with AUC ≈ 0.5 (average performance)
  - 2 classes with AUC < 0.5 (low performance)
  - 21 classes with AUC = 1.0 (excellent classification)

---

## 💡 Challenges & Improvements

- **Challenge**: Strong class imbalance affected overall performance.
- **Future Improvements**:
  - Use of more powerful models (e.g., BERT or AraBERT)
  - Better class balancing strategies (SMOTE, oversampling)
  - Advanced NLP techniques tailored for Arabic

---

## 🛠️ Technologies Used

- Python
- Scikit-learn
- Tashaphyne (Arabic NLP)
- BeautifulSoup / Selenium (for web scraping)
- Jupyter Notebook

---

## 🚀 How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/Nadaaaaaaaaaaaaaaaaaa/arabic-quotes-classification.git
   cd arabic-quotes-classification
Create a virtual environment and install dependencies:

bash
Copier le code
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
Run preprocessing and training notebooks:

01_scraping.ipynb

02_preprocessing.ipynb

03_training_model.ipynb

🌟 Project Highlights
One of the first projects focusing on multi-class classification of Arabic quotes.

Tackled Arabic language complexity with tailored preprocessing.

Dataset and code publicly available for future research.

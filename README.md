# Measuring Bias in Crowdsourced Datasets using PMI

*A hands-on project exploring how stereotypes emerge in crowdsourced text datasets.*

---

## 📌 **Project Overview**

Crowdsourced datasets—such as those collected from Mechanical Turk or open community platforms—often contain subtle but harmful biases against social groups. These biases propagate into models trained on these datasets, influencing predictions and downstream AI behavior.

This project analyzes **how stereotypes form in crowdsourced text data** using **Pointwise Mutual Information (PMI)** as a measure of association strength between:

* **Target groups** (e.g., gender, race, professions)
* **Descriptive terms or attributes** (e.g., "violent", “intelligent”, “emotional”, etc.)

The notebook walks through loading the dataset, preprocessing text, computing PMI, and interpreting which group–attribute pairings reveal potential bias.

---

## 🎯 **Objectives**

* Understand how linguistic bias is embedded in text datasets.
* Apply **PMI** to quantify association strength between groups and attributes.
* Identify **positive and negative stereotypes** emerging from crowdsourced responses.
* Visualize bias patterns using tables and plots.
* Discuss implications for dataset quality and ethical AI development.

---

## 🧠 **What is PMI?**

**Pointwise Mutual Information (PMI)** measures how much more frequently two words appear together than expected by chance.

[
PMI(x, y) = \log \frac{P(x,y)}{P(x)P(y)}
]

* **PMI > 0** → occurs together more than expected → potential stereotype
* **PMI < 0** → occurs together less than expected
* **PMI = 0** → independent
* Higher absolute PMI values reflect stronger associations (positive or negative)

---

## 📂 **Project Structure**

```
├── biasInCrowdsourcedDataset_v2.ipynb   # Main notebook
├── data/                                # Raw dataset folder
├── README.md                            # Project documentation
└── requirements.txt                     # Python dependencies (if added)
```

---

## ⚙️ **Key Steps in the Notebook**

1. **Load and inspect the dataset**

   * Review structure, column names, text fields.
2. **Preprocess text**

   * Tokenization
   * Lowercasing
   * Stopword removal
3. **Define target groups and attribute lists**
4. **Compute PMI values**

   * Frequency counts
   * Joint probabilities
   * PMI matrix or table
5. **Visualize results**

   * Heatmaps
   * Bar graphs
6. **Interpret bias patterns**

   * Which groups receive disproportionately negative/positive attributes?
   * Are stereotypes amplified in crowdsourced text?
7. **Discussion on ethical implications**

   * Dataset curation
   * Model impact
   * Mitigation strategies

---

## 📊 **Example Outputs**

* PMI heatmaps showing associations
* Top-k stereotypical word associations
* Group-wise comparison charts
* Tables listing strongest positive/negative PMI values

---

## 🛠️ **Tech Stack**

* **Python**
* pandas
* numpy
* nltk / spaCy
* matplotlib / seaborn
* scikit-learn
* Jupyter Notebook

---

## 🧩 **How to Run**

1. Clone the repo:

   ```bash
   git clone https://github.com/samyuktha-pillai/Bias_in_Crowdsourced_Datasets.git
   cd yourrepo
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook:

   ```bash
   jupyter notebook biasInCrowdsourcedDataset_v2.ipynb
   ```

---

## ✨ **Key Insights**

* Crowdsourced datasets can unintentionally encode **stereotypical associations**.
* PMI is a simple but powerful tool for **quantifying linguistic bias**.
* Bias detection is essential before using datasets for training ML models.
* Understanding these patterns helps move toward **fairer and more responsible AI**.

---

## 📘 **Future Work**

* Extend analysis to contextual embeddings (e.g., BERT).
* Use PMI variants: normalized PMI (nPMI).
* Run significance testing on associations.
* Apply debiasing methods to reduce harmful correlations.

---

## 🤝 **Contributions**

Pull requests are welcome!
Feel free to open an issue for improvements, bugs, or feature suggestions.

---

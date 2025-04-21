
# Unveiling Gender Bias in Occupations with Word Embeddings

## 📌 Project Overview
This project investigates **gender bias** in pre-trained **GloVe word embeddings** related to occupational terms, aiming to uncover hidden societal stereotypes encoded in language models. Using publicly available datasets, it employs techniques such as **gender direction projection**, **analogy tests**, and the **Word Embedding Association Test (WEAT)** to quantify bias.

The results are compared with real-world gender ratios from the **U.S. Bureau of Labor Statistics (BLS)** to validate observed patterns. The entire project is designed to run within a **Kaggle notebook**, ensuring accessibility and reproducibility.

---

## 🎯 Objectives

- Quantify gender bias in GloVe embeddings for occupational terms.
- Correlate detected biases with actual gender distributions in the U.S. workforce.
- Provide a reproducible framework for bias analysis in word embeddings.
- Contribute to AI ethics by highlighting implications of biased language models.

---

## 🧠 Hypothesis

> Word embeddings, derived from human-written texts, encode gender biases in occupational contexts that can be extracted and correlated with real-world workforce gender distributions.

---

## 📊 Datasets

- **GloVe Word Embeddings**  
  Pre-trained GloVe vectors (6B tokens, 300 dimensions) from Kaggle.  
  **[Link: GloVe Global Vectors for Word Representation](https://www.kaggle.com/datasets/)**

- **BLS Occupational Data**  
  Gender ratios by occupation from the U.S. Bureau of Labor Statistics’ *Current Population Survey (CPS)* – 2024 Annual Averages.  
  **[Link: BLS CPS Table 11](https://www.bls.gov/cps/cpsaat11.htm)**

---

## ⚙️ Methodology

The project is implemented in Python via a Kaggle notebook and consists of the following steps:

1. **Load Embeddings**: Import GloVe vectors using `gensim`.
2. **Process BLS Data**: Extract occupation names and gender ratios with `pandas`.
3. **Define Gender Direction**: Calculate a gender direction vector using word pairs (e.g., *“man” – “woman”*).
4. **Calculate Bias Scores**: Project occupation vectors onto the gender direction.
5. **Analyze Correlations**: Use `scipy` to correlate bias scores with BLS gender ratios.
6. **Conduct Analogy Tests**: Perform analogy completions for selected occupations.
7. **Implement WEAT**: Run the Word Embedding Association Test for deeper bias quantification.
8. **Visualize Results**: Create scatter plots, histograms, and other visualizations with `matplotlib`.

---

## 🛠 Tools and Libraries

- `gensim`, `pandas`, `numpy`, `scipy`, `matplotlib`
- **Environment**: Kaggle Notebook (cloud-based and free)

---

## 🚀 Installation and Setup

1. **Create a Kaggle Notebook**  
   Navigate to [Kaggle](https://www.kaggle.com/) and create a new notebook.

2. **Add Datasets**  
   - Add the GloVe dataset from Kaggle Datasets.
   - Download BLS CPS Table 11 from the BLS website and upload it to the notebook.

3. **Install Dependencies**  
   Most libraries are pre-installed. If necessary, run:  
   ```bash
   !pip install gensim pandas numpy scipy matplotlib
   ```

4. **Run the Notebook**  
   - Copy the project code into the notebook.
   - Execute all cells in sequence to preprocess, analyze, and visualize results.

---

## 📁 Project Structure

```
gender_bias_embeddings.ipynb         # Main notebook with code and documentation
/kaggle/input/
  └─ glove-global-vectors...         # Pre-trained GloVe embeddings
cpsaat11.xlsx                        # BLS gender ratio data (uploaded manually)
/output/
  ├─ bias_scores.png
  ├─ correlation_plot.png
  └─ summary.md                      # Summary of results
```

---

## 📈 Usage Instructions

1. Open the Kaggle notebook.
2. Ensure both datasets (GloVe and BLS) are available.
3. Run all cells to:
   - Load and preprocess data
   - Compute bias scores and correlations
   - Perform analogy tests and WEAT
   - Generate visualizations
4. Review outputs in cells and saved images.

---

## ✅ Expected Results

- **Bias scores** indicating male or female associations per occupation.
- **Correlation** between bias scores and gender ratios in the workforce.
- **Analogy completions** (e.g., *“man:engineer :: woman:nurse”*) exposing stereotypes.
- **WEAT scores** quantifying differential associations.

---

## ⚠️ Limitations

- Dependence on static GloVe embeddings may miss context-specific nuances.
- BLS data may oversimplify occupational categories.
- GloVe is trained on general-purpose corpora, introducing unrelated noise.

---

## 🔮 Future Work

- Integrate **contextual embeddings** (e.g., BERT) for deeper analysis.
- Apply **debiasing algorithms** to mitigate detected bias.
- Expand analysis to include **race**, **age**, and other demographic factors.

---

## 📚 Citation

If you use this project or its code, please cite:

- GloVe: Global Vectors for Word Representation  
- BLS CPS Table 11  
- Kaggle GloVe Dataset

---

## 🙏 Acknowledgments

This project builds upon foundational work by:
- **Bolukbasi et al. (2016)** – *Man is to Computer Programmer as Woman is to Homemaker*
- **Caliskan et al. (2017)** – *Semantics derived automatically from language corpora contain human-like biases*

Datasets are sourced from **Kaggle** and the **U.S. Bureau of Labor Statistics**.

---

## 📬 Contact

For questions or collaboration, reach out via **[Kaggle profile]** or **[email]**.
```

# Walmart Black Friday Sales Analysis: Unlocking Customer Insights for Smarter Retail Strategies

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.5%2B-yellow?logo=pandas&logoColor=black)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.12%2B-orange?logo=seaborn&logoColor=white)](https://seaborn.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Stars](https://img.shields.io/github/stars/username/walmart-analysis?style=social)](https://github.com/username/walmart-analysis)

---

## 🚀 **Project Overview**

This project dives deep into Walmart's Black Friday sales data to uncover hidden patterns in customer purchase behavior. By analyzing over **550,000 transactions**, we explore how factors like **gender**, **age**, **marital status**, and **product categories** influence spending habits. The goal? Empower retail giants like Walmart with data-driven insights to optimize marketing, personalize recommendations, and boost revenue.

Key Questions Answered:
- Do women spend more than men on Black Friday?
- How does age shape product preferences and basket sizes?
- Can marital status predict spending power?

Armed with **exploratory data analysis (EDA)**, **statistical hypothesis testing**, and **bootstrapping simulations**, this analysis reveals actionable strategies—such as targeted upselling for high-spending male segments and budget bundles for young shoppers.

Perfect for data enthusiasts, aspiring data scientists, or retail analysts looking to blend storytelling with stats!

---

## 📊 **Key Features & Insights**

- **Demographic Deep Dive**: Quantified spending differences—males average ₹9,438 vs. females' ₹8,735 (95% CI non-overlapping).
- **Statistical Rigor**: Chi-square tests (p < 0.001) confirm gender-product associations; two-way ANOVA highlights age-marital interactions.
- **Central Limit Theorem in Action**: Bootstrapped confidence intervals across sample sizes (300–550K) to validate findings.
- **Business Impact**: Recommendations include gender-tailored promotions (e.g., electronics for men) and age-segmented campaigns (e.g., premium deals for 51-55 group).

| Demographic | Avg. Spend (₹) | Key Preference | Stat. Significance |
|-------------|----------------|----------------|---------------------|
| **Male**    | 9,438         | Product Cat. 1 | p < 0.001 (Chi²)   |
| **Female**  | 8,735         | Product Cat. 5 |                     |
| **0-17**    | 8,933         | Product Cat. 5 | p < 1e-49 (ANOVA)  |
| **51-55**   | 9,535         | Product Cat. 8 |                     |
| **Married** | 9,261         | Neutral        | No sig. diff.      |

---

## 🛠 **Tech Stack**

- **Languages & Frameworks**: Python 3.8+
- **Data Manipulation**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Statistics**: SciPy (Chi-square, normality), Statsmodels (ANOVA)
- **Environment**: Jupyter Notebook (for interactive analysis)

---

## 📁 **Dataset**

Sourced from a public Kaggle dataset simulating Walmart's Black Friday sales (50M male + 50M female customers assumed).

- **Size**: 550,068 rows × 10 columns
- **Columns**:
  - `User_ID`, `Product_ID`: Identifiers
  - `Gender`, `Age`, `Marital_Status`: Demographics
  - `Occupation`, `City_Category`, `Stay_In_Current_City_Years`: Lifestyle factors
  - `Product_Category`: Item type (1-20)
  - `Purchase`: Transaction amount (target variable)

Download via:
```bash
!gdown 15M27gosWyUG1I_2wA-czk2bsflbpYbyv  # walmart_data.csv
```

No nulls detected; minor outliers in `Purchase` retained for realism.

---

## 🏗 **Getting Started**

### Prerequisites
- Python 3.8+
- Jupyter Notebook or Google Colab

### Installation
1. Clone the repo:
   ```bash
   git clone https://github.com/username/walmart-analysis.git
   cd walmart-analysis
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   (Includes: pandas, numpy, matplotlib, seaborn, scipy, statsmodels)

3. Download the dataset (or use the provided script in `data/`).

### Running the Analysis
1. Launch Jupyter:
   ```bash
   jupyter notebook Walmart_Analysis.ipynb
   ```

2. Execute cells sequentially for EDA, stats, and visualizations.

Expected runtime: ~5-10 minutes on standard hardware.

---

## 📈 **Analysis Workflow**

1. **Data Import & EDA**:
   - Load CSV with Pandas.
   - Explore distributions (e.g., age groups: 26-35 dominates at 40%).

2. **Visualizations**:
   - Count plots for occupations, ages, product categories.
   - Heatmaps for age-product crosstabs.
   - Histograms & boxplots for purchase outliers.

3. **Hypothesis Testing**:
   - **Chi-square**: Age-product (p=0) and gender-product associations.
   - **Two-way ANOVA**: Age × Marital_Status on Purchase (all p < 1e-22).

4. **CLT & Bootstrapping**:
   - Simulated 10K samples for 95% CIs at sizes 300–full N.
   - Key: CI widths shrink with larger samples; non-overlap confirms gender gap.

5. **Insights & Recommendations**:
   - Target males with high-value upsells; females with category bundles.
   - Age-stratified: Budget for teens, premium for seniors.

Sample Plot: Age-Product Heatmap
![Age-Product Heatmap](assets/age_product_heatmap.png) <!-- Add actual image path -->

---

## 📝 **Key Findings Summary**

- **Gender Gap**: Males outspend females by ~8%; leverage for personalized ads.
- **Age Dynamics**: 51-55 group highest spenders; 0-17 lowest—tailor accordingly.
- **Marital Neutrality**: No direct impact; use in combo with age.
- **Product Trends**: Cat. 5 (youth fave), Cat. 8 (senior pick).

Full report in `report/` folder or Jupyter output.

---

## 🤝 **Contributing**

Love retail analytics? Fork the repo, add features (e.g., ML predictions), or fix bugs!

1. Fork & clone.
2. Create a branch: `git checkout -b feature/amazing-feature`.
3. Commit: `git commit -m "Add amazing feature"`.
4. Push & PR!

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

---

## 📄 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 **Author & Connect**

Built with ❤️ by [Your Name] (@yourusername on GitHub/Twitter).

- 📧 Email: your.email@example.com
- 🔗 Portfolio: [yourwebsite.com](https://yourwebsite.com)
- 💼 LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)

Star ⭐ this repo if it sparks ideas—let's connect on data adventures!

---

*Last Updated: November 28, 2025*  
*Inspired by real-world retail challenges—data for good!*

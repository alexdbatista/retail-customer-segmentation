# RFM Customer Segmentation Analysis
## Translating Analytical Chemistry Rigor to Business Intelligence

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Author:** Alex Domingues Batista, PhD  
**Background:** Analytical Chemistry | 16+ years research experience  
**Project Type:** Portfolio demonstration of statistical validation & methodological rigor

---

## 📊 Project Overview

This project applies **PhD-level statistical validation methods** from analytical science to customer behavior analysis. Rather than following a standard RFM tutorial, this analysis demonstrates:

- ✅ **Method validation** (RFM quartiles vs k-means clustering)
- ✅ **Sensitivity analysis** (quartile vs quintile binning stability testing)
- ✅ **Assumption testing** (correlation analysis, distribution assessment)
- ✅ **Transparent documentation** (exploratory dead-ends included)
- ✅ **Reproducible research** (clear methodology, all code provided)

**Dataset:** UCI Online Retail Dataset (~540K transactions, 13 months, UK e-commerce)

---

## 🎯 Key Results

| Metric | Finding |
|--------|---------|
| **Customer Base** | 4,372 registered customers segmented into 5 groups |
| **Revenue Concentration** | Top 25% (Champions) contribute ~60% of total revenue |
| **Statistical Validation** | ANOVA confirms segments are significantly distinct (p < 0.001) |
| **Method Agreement** | 70-80% agreement between RFM and k-means approaches |
| **Stability** | >80% segment assignment stability across binning methods |
| **CLV Range** | Champions: £6,732 avg vs Hibernating: £222 avg (30x difference) |

---

## 🔬 What Makes This PhD-Level?

### 1. **Methodological Comparison**
- Implemented both RFM quartile scoring AND k-means clustering
- Cross-validated segment assignments between methods
- Calculated silhouette scores and agreement metrics
- **Conclusion:** RFM captures natural data structure (not arbitrary)

### 2. **Sensitivity Analysis**
- Tested robustness by varying binning approach (quartiles → quintiles)
- Measured segment stability (% customers with same assignment)
- **Result:** High stability validates methodological choice

### 3. **Exploratory Dead-Ends**
- Documented transformations that didn't improve results (log scaling)
- Tested independence assumptions (correlation analysis)
- **Why show failures?** Authentic research process, not polished tutorial

### 4. **Assumption Validation**
- Assessed multicollinearity between RFM dimensions
- Evaluated distribution skewness and outlier impact
- Justified quartile approach despite moderate F-M correlation (r ~0.6)

---

## 🛠️ Technical Stack

**Core Libraries:**
- `pandas`, `numpy` - Data manipulation
- `scipy` - Statistical testing (ANOVA, t-tests, Pearson correlation)
- `scikit-learn` - K-means clustering, StandardScaler, silhouette analysis
- `matplotlib`, `seaborn` - Visualization

**Statistical Methods:**
- RFM quartile/quintile binning
- One-way ANOVA (segment validation)
- Independent t-tests (Champions vs Hibernating)
- K-means clustering (k=5)
- Pearson correlation analysis
- Silhouette coefficient

---

## 📁 Project Structure

```
retail-customer-segmentation/
│
├── RFM_Customer_Segmentation.ipynb  # Main analysis notebook
├── README.md                         # This file
├── .gitignore                        # Excludes data files
└── Online Retail.xlsx                # Data (not in repo - see below)
```

---

## 🚀 How to Run

### 1. **Clone the Repository**
```bash
git clone https://github.com/alexdbatista/retail-customer-segmentation.git
cd retail-customer-segmentation
```

### 2. **Download the Dataset**
The dataset is not included in this repository due to size constraints.

📥 **Download:** [UCI Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)
- File: `Online Retail.xlsx`
- Place in project root directory

### 3. **Install Dependencies**
```bash
pip install pandas numpy scipy scikit-learn matplotlib seaborn openpyxl
```

### 4. **Run the Notebook**
```bash
jupyter notebook RFM_Customer_Segmentation.ipynb
```

---

## 📈 Business Applications

**Segment-Specific Strategies:**

| Segment | % Customers | % Revenue | Action |
|---------|-------------|-----------|--------|
| **Champions** | 25% | 60% | VIP programs, early access, retention focus |
| **Loyal Customers** | 23% | 25% | Cross-sell campaigns, referral programs |
| **Potential Loyalists** | 18% | 10% | Engagement sequences, purchase incentives |
| **At Risk** | 20% | 4% | Win-back campaigns, churn analysis |
| **Hibernating** | 14% | <1% | Low-cost re-engagement or suppression |

---

## 🔍 Project Highlights

### Scientific Rigor Applied to Business Problem
After 16 years in analytical chemistry research, this project demonstrates how experimental design, hypothesis testing, and method validation principles translate directly to business analytics:

- **Data Quality → Sample Preparation:** Rigorous cleaning (removed 25% invalid records)
- **Method Development → Segmentation Validation:** Compared RFM vs k-means
- **Quality Control → Sensitivity Analysis:** Tested parameter robustness
- **Lab Notebook → Documentation:** Transparent reporting of exploratory paths

### Key Analytical Decisions

1. **Why quartiles, not k-means?**  
   Both methods agree (~75%), but quartiles are interpretable for stakeholders

2. **Why not log-transform skewed data?**  
   Tested and rejected—doesn't improve segmentation, reduces interpretability

3. **How do you handle F-M correlation?**  
   Acknowledged but acceptable trade-off for business alignment

---

## 📊 Sample Visualizations

The notebook includes:
- 📉 Distribution analysis (histograms, box plots)
- 🎨 3D scatter plot of RFM space
- 🔥 Heatmaps (segment profiles, correlations)
- 📊 Revenue contribution charts
- 🧪 Method comparison visualizations

---

## 🎓 About the Author

**Alex Domingues Batista, PhD**  
- 16+ years analytical chemistry research
- Expertise in statistical validation, method development, hypothesis testing
- Transitioning to data science/analytics
- Applying research rigor to business problems

**Connect:**
- GitHub: [@alexdbatista](https://github.com/alexdbatista)
- LinkedIn: [Add your LinkedIn]

---

## 📝 License

This project is open source and available under the MIT License.

---

## 🙏 Acknowledgments

- **Data Source:** UCI Machine Learning Repository - Online Retail Dataset
- **Inspiration:** Translating 16 years of analytical method validation to business intelligence
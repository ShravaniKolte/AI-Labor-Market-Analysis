# AI-Labor-Market-Analysis

Which human skills will survive the AI revolution — and which are already obsolete?

<img width="700" height="500" alt="automation_risk_distribution" src="https://github.com/user-attachments/assets/b21b2c88-fefd-4f0e-aebc-cce228a35d8b" />
<img width="700" height="500" alt="ai_adoption_stage" src="https://github.com/user-attachments/assets/c952e224-fbbe-4887-8406-4319afda9b04" />


📌 Project Overview

As AI and automation continue to reshape the global workforce, understanding which skills are future-proof versus at risk of obsolescence has never been more critical. This project builds a data-driven framework to analyze skill survival probability across industries from 2010 to 2030 — combining historical labor data, automation risk indicators, and a custom-designed weighted scoring model.
The findings reveal that 73% of analyzed skills are classified as at-risk or likely obsolete by 2030, underscoring the urgency for upskilling and workforce transformation.

🎯 Problem Statement

With AI-driven disruption accelerating across sectors, workers, educators, and policymakers lack a clear, data-backed view of which skills will remain relevant in the future labor market. This project addresses:

Which skill categories face the highest automation risk?
How has the demand for different skills shifted from 2010 to 2030?
Can we build a Skill Survival Probability model to classify skills into actionable categories?


📂 Dataset

**Key columns include:**
- `skill_name` — Name of the skill (e.g., Data Analysis, Welding, Copywriting)
- `skill_category` — Broad category: Technical, Cognitive, Physical, or Social
- `industry` — Industry sector the skill belongs to
- `automation_risk_score` — Likelihood of automation on a 0–1 scale
- `demand_growth_rate` — Year-over-year demand change (%)
- `adaptability_score` — How easily the skill adapts to new contexts
- `ai_complementarity` — Degree to which AI augments rather than replaces the skill
- `survival_probability` — Weighted composite score from 0 to 100
- `survival_label` — Final classification: Future-Proof / Stable / At-Risk / Likely Obsolete

---

## 🔧 Methodology

### 1. Data Cleaning
- Handled missing values via median imputation and category-mode fill
- Removed outliers using IQR-based filtering
- Standardized column names and data types
- Feature engineering: derived `survival_probability` from weighted sub-scores

### 2. Exploratory Data Analysis (EDA)
9 charts covering:
- Distribution of survival labels across skill categories
- Automation risk by industry
- Demand growth trends (2010 vs 2030)
- Correlation heatmap of key features
- Top 10 future-proof vs. top 10 likely-obsolete skills
- Skill adaptability vs. AI complementarity scatter plot

### 3. Skill Survival Probability Model

A custom weighted scoring formula was designed to classify each skill:

```
Survival Probability =
  (0.35 × AI Complementarity Score)
+ (0.25 × Demand Growth Rate — normalized)
+ (0.20 × Adaptability Score)
+ (0.20 × (1 — Automation Risk Score))
```

### 4. Classification Labels

Skills were classified into four categories based on their survival score:

- 🟢 **Future-Proof (75–100)** — High demand, AI-augmented, highly adaptable
- 🟡 **Stable (50–74)** — Moderate risk, demand holding steady
- 🟠 **At-Risk (25–49)** — Significant automation exposure, declining demand
- 🔴 **Likely Obsolete (0–24)** — High automation risk, steep demand decline

---

## 📊 Key Findings

- **73%** of all analyzed skills are classified as At-Risk or Likely Obsolete by 2030
- Technical and Cognitive skills show the highest future-proof rates
- Physical and Routine skills face the greatest obsolescence pressure
- Skills with high AI complementarity (e.g., critical thinking, data interpretation) show strong survival regardless of industry
- The Manufacturing and Administrative sectors are most exposed to automation risk
- Healthcare and Creative sectors show the most resilient skill profiles

---

## 🖥️ Power BI Dashboard

An interactive Power BI dashboard was built with a custom purple theme, featuring:

- KPI cards showing total skills analyzed, % future-proof, and % at-risk
- Bar chart of skill survival distribution by category
- Industry-level automation risk heatmap
- Demand trend line from 2010 to 2030
- Slicers to filter by industry, skill category, and survival label

> Dashboard screenshots available in the `/assets` folder.

---

## 🛠️ Tools & Technologies

- **Python 3.10** — Data cleaning, EDA, model logic
- **Pandas & NumPy** — Data manipulation
- **Matplotlib & Seaborn** — EDA visualizations
- **Google Colab** — Development environment
- **Power BI** — Interactive dashboard
- **GitHub** — Version control & portfolio hosting

---

## 📁 Project Structure

```
ai-labor-market-analysis/
│
├── data/
│   ├── raw_skill_data.csv              # Original dataset
│   └── cleaned_skill_data.csv          # Post-cleaning dataset
│
├── notebooks/
│   └── skill_survival_analysis.ipynb   # Full Colab notebook
│
├── dashboard/
│   └── skill_survival_dashboard.pbix   # Power BI file
│
├── assets/
│   └── dashboard_screenshot.png        # Dashboard preview
│
└── README.md
```

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/ShravaniKolte/ai-labor-market-analysis.git
   cd ai-labor-market-analysis
   ```

2. **Open the notebook in Google Colab**
   - Upload `notebooks/skill_survival_analysis.ipynb` to [colab.research.google.com](https://colab.research.google.com)
   - Run all cells sequentially

3. **View the dashboard**
   - Open `dashboard/skill_survival_dashboard.pbix` in Power BI Desktop

---

## 💡 Future Scope

- Add a machine learning classifier (Random Forest / Logistic Regression) to validate the weighted model
- Integrate real-time job posting data via LinkedIn/Indeed APIs
- Build a web app where users can input a skill and get its survival score
- Expand dataset to cover regional/country-level labor market differences

---

## 👩‍💻 Author

**Shravani Kolte**
B.Tech — Robotics & Automation | Zeal College of Engineering & Research, Pune
Aspiring Data Analyst | Python • SQL • Power BI

[![GitHub](https://img.shields.io/badge/GitHub-ShravaniKolte-black?style=flat-square&logo=github)](https://github.com/ShravaniKolte)

---

*If you found this project useful or interesting, consider giving it a ⭐ on GitHub!*


PropertyDetailsRows5,000Columns22Time Span2010 – 2030SourceCustom-engineered dataset (synthetic + research-backed)

If you found this project useful or interesting, consider giving it a ⭐ on GitHub!

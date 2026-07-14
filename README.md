<div align="center">

# 🧑‍💼 IBM HR Attrition Analysis
### Interactive Tableau Dashboard — *Why Are Employees Leaving?* 🚪📉

![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)
![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)
![CSV](https://img.shields.io/badge/Data-CSV-4CAF50?style=for-the-badge&logo=googlesheets&logoColor=white)
![GitHub](https://img.shields.io/badge/Repo-GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

**🔗 [View the Live Dashboard on Tableau Public →](https://public.tableau.com/app/profile/m.j4179/viz/IBMHRAttributionAnalysisDashboard/Dashboard1?publish=yes)**

</div>

---

## 🧭 Table of Contents
- [📌 Objective](#-objective)
- [🗂️ Dataset](#️-dataset)
- [📊 Dashboard Preview](#-dashboard-preview)
- [🔎 Key Insights](#-key-insights)
- [🧩 Dashboard Features](#-dashboard-features)
- [🛠️ Tools & Tech Stack](#️-tools--tech-stack)
- [📁 Repository Structure](#-repository-structure)
- [▶️ How to Reproduce](#️-how-to-reproduce)
- [⚠️ Limitations](#️-limitations)
- [👤 Author](#-author)

---

## 📌 Objective

> 💡 **Why are employees leaving, and which factors correlate most strongly with attrition?**

Instead of one static answer, this dashboard hands the wheel to the viewer 🎛️ — filter by department, age bracket, or role, and instantly see which drivers (overtime ⏰, income 💰, tenure 📆, satisfaction 😀, commute 🚗) matter most for *that specific slice* of the workforce.

---

## 🗂️ Dataset

| | |
|---|---|
| 📦 **Source** | [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) (Kaggle) |
| 🧮 **Size** | 1,470 employees × 35 fields |
| 🎯 **Target variable** | `Attrition` (Yes / No) |
| 🏷️ **Type** | Fictional data, created by IBM data scientists |

> ℹ️ **Note:** this dataset has no geographic *Region* field — `Department` and `Job Role` stand in as the organizational-region filters instead.

---

## 📊 Dashboard Preview

*(Drop your final dashboard screenshot here 👇)*
<img width="1702" height="855" alt="Dashboard 2" src="https://github.com/user-attachments/assets/26474b5c-a157-4211-b5a8-571b323d3c27" />

```markdown
![Dashboard Preview](assets/dashboard_preview.png)
```

---

## 🔎 Key Insights

Based on the full, unfiltered dataset:

- ⏰ **Overtime is the #1 behavioral driver** — employees who work overtime leave at roughly **3x the rate** of those who don't (~30.5% vs ~10.4%).
- 🧑‍💻 **Sales Representatives are the highest-risk role** (~40% attrition), while **Research Directors** are the most stable (~2.5%).
- 🎂 **Attrition skews young** — the 18–24 age group leaves at nearly **40%**, dropping steadily with every older bracket.
- 💍 **Single employees churn more** than married or divorced employees.
- 😀 **Satisfaction and attrition move inversely** — "Low" job satisfaction shows a noticeably higher exit rate than "Very High."
- 💸 **Pay gaps widen at senior levels** — employees who left tend to earn less than peers who stayed, and the gap grows at higher job levels.

> 🧠 These are *patterns*, not proof of causation — correlation ≠ causation. See [Limitations](#️-limitations).

---

## 🧩 Dashboard Features

### 🎚️ Global Filters
*(apply to every chart at once)*

🏢 Department &nbsp;·&nbsp; 🎂 Age Group &nbsp;·&nbsp; 🧑‍💼 Job Role &nbsp;·&nbsp; ⏰ OverTime &nbsp;·&nbsp; 💍 Marital Status

### 🏆 KPI Summary Strip
| 👥 Total Employees | 📉 Attrition Rate | 💰 Avg. Monthly Income | 📆 Avg. Years at Company |
|---|---|---|---|

### 📈 Charts

| Chart | Question it Answers |
|---|---|
| 🏢 Attrition by Department | Which departments lose the most people? |
| 🎂 Attrition by Age Group | Which career stage is highest-risk? |
| ⏰ OverTime vs. Attrition | Does overtime status predict attrition? |
| 💰 Income by Job Level & Attrition | Is pay a factor, and at which levels? |
| 😀 Attrition by Job Satisfaction | Does self-reported satisfaction track with leaving? |
| 🚗 Distance From Home by Job Role | Does commute distance differ for leavers vs. stayers? |
| 🧑‍💼 Attrition Rate by Job Role | Which specific roles are highest/lowest risk? |

---

## 🛠️ Tools & Tech Stack

<div align="center">

| Tool | Purpose |
|:---:|---|
| <img src="https://cdn.simpleicons.org/tableau/E97627" width="28"/> **Tableau Public** | Dashboard authoring, calculated fields & publishing |
| <img src="https://cdn.simpleicons.org/kaggle/20BEFF" width="28"/> **Kaggle** | Source of the IBM HR Attrition dataset |
| <img src="https://cdn.simpleicons.org/googlesheets/34A853" width="28"/> **CSV** | Raw tabular data format |
| <img src="https://cdn.simpleicons.org/github/181717" width="28"/> **GitHub** | Version control & project hosting |

</div>

**⚙️ Calculated fields built for this dashboard:**
- `🚩 Attrition Flag` — converts Yes/No into 1/0 so attrition can be averaged into a rate
- `🎂 Age Group` — bins raw `Age` into five brackets
- `🏷️ Job Satisfaction Label` / `Work Life Balance Label` / `Environment Satisfaction Label` / `Job Involvement Label` — map IBM's 1–4 ordinal codes to readable text
- `🚗 Distance If Left` — isolates commute distance only for employees who left, so roles are ranked by *that* signal rather than a blended average

**🔗 Interactivity:** Dashboard actions + `Apply to Worksheets → All Using This Data Source` filters for full cross-chart filtering.

---

## 📁 Repository Structure

```
📦 HR-Attrition-Dashboard
├── 📂 data/
│   └── 📄 WA_Fn-UseC_-HR-Employee-Attrition.csv   # Raw IBM dataset
├── 📂 assets/
│   └── 🖼️ dashboard_preview.png                    # Screenshot of the published dashboard
├── 📊 HR_Attrition_Dashboard.twbx                  # Packaged Tableau workbook
└── 📘 README.md
```

---

## ▶️ How to Reproduce

1. ⬇️ Download [Tableau Public](https://www.tableau.com/products/public/download) — it's free.
2. 📂 Open `HR_Attrition_Dashboard.twbx`, or connect fresh to `data/WA_Fn-UseC_-HR-Employee-Attrition.csv`.
3. 🧮 Recreate the calculated fields listed under [Tools & Tech Stack](#️-tools--tech-stack).
4. 🏗️ Build each worksheet and assemble the dashboard — or just open the packaged `.twbx` to explore the finished version directly.

---

## ⚠️ Limitations

- 🎭 This is a **fictional dataset**, generated by IBM for demonstration — findings shouldn't be generalized to real organizations.
- 🔬 Small filtered subgroups (e.g., one job role + one age bracket) can rest on very few employees — read those rates cautiously.
- 🔗 Correlational patterns (e.g., overtime ↔ attrition) do **not** establish causation.

---

## 👤 Author

<div align="center">

**Mayank Jaiswal**
🎓 Data Analyst Intern · Data Analytics & Visualization


⭐ *If this project was useful, consider giving it a star!*

</div>

# 📊 Excel Dashboard Collection

A curated set of professional **Excel dashboards** built with dark-themed styling, live formulas, and interactive data tables — covering HR analytics, QA engineering, and resource/budget estimation.

---

## 📁 File Overview

### 🧑‍💼 HR Analytics Dashboards

| File | Description |
|------|-------------|
| `Excel_Dashboard_Tutorial.xlsx` | Master tutorial workbook — step-by-step guide to building Excel dashboards |
| `Dashboard1_HR_Overview.xlsx` | High-level HR metrics: headcount, turnover, open roles, and workforce KPIs |
| `Dashboard2_Salary_Analysis.xlsx` | Salary distribution by department, role, and band with quartile breakdowns |
| `Dashboard3_Demographics.xlsx` | Workforce diversity metrics: gender, age groups, education, and ethnicity |
| `Dashboard4_JobTitle.xlsx` | Headcount and salary analysis by job title and grade level |
| `Dashboard5_Tenure.xlsx` | Employee tenure distribution, average tenure by department, and retention trends |
| `Dashboard6_Employee.xlsx` | Individual employee-level data explorer with filters and summary KPIs |

---

### 🧪 QA Engineering Dashboards

| File | Description |
|------|-------------|
| `QA_Dashboard.xlsx` | Full Software QA tracking dashboard: bug tracker, test runs, tester scorecard, and sprint health |
| `QA_Estimation_Template.xlsx` | **Reusable QA Resource & Budget Estimation Template** (see details below) |

---

## 📐 QA Estimation Template — Sheet Guide

`QA_Estimation_Template.xlsx` is a **multi-technique estimation workbook** designed for QA Managers to plan resources and budgets across projects. It applies five industry-standard estimation techniques in one file.

### Sheets

| Sheet | Technique / Purpose |
|-------|---------------------|
| 📋 **Estimation Dashboard** | Master summary — KPI cards, side-by-side technique comparison, risk buffer, and final recommended estimate |
| ⚙️ **Config** | Project setup: name, release, dates, QA lead, and full team roster with roles, skill levels, hourly rates, and sprint allocations |
| 📊 **PERT Estimation** | Phase-level **PERT** estimates: enter Optimistic / Most Likely / Pessimistic hours per QA phase → auto-calculates PERT hours, Std Dev, and 95% confidence interval |
| 🔺 **Three-Point** | Feature-level **Three-Point** estimates: both PERT and Triangular averages with confidence bands per user story or feature |
| 🃏 **Story Points** | **Agile Story Point** estimation: assign Fibonacci story points per epic/story, set team velocity and hours-per-point → QA hour totals with actuals tracking |
| 🔍 **Analogy** | **Analogy-Based** estimation: compare against past reference projects using complexity factors and similarity weighting → weighted average estimate |
| 📐 **UCP** | **Use Case Point (UCP)** method: log use cases with complexity weights, set TCF/ECF adjustment factors and productivity rate → total QA hours |
| 📝 **Test Planning** | Requirements-driven **test case estimation**: configure test-to-requirement ratio and hours per case → design, execution, regression, and total hours |
| 💰 **Budget Planner** | Full **QA budget calculator**: labor costs (pulled from Config), tools, infrastructure, training, and contingency → final recommended budget |
| 📅 **Sprint Resource Plan** | **Sprint-by-sprint allocation**: track planned vs. actual hours, assigned testers, test cases, pass rates, and bugs found per sprint |
| 📖 **How to Use** | Step-by-step usage guide for all sheets |

### How to Use

1. **Open** `QA_Estimation_Template.xlsx`
2. **Start with ⚙️ Config** — fill in project details and team roster (dark green cells are user inputs)
3. **Fill in estimation sheets** (PERT, Three-Point, Story Points, Analogy, UCP) with your project data
4. **Review 📝 Test Planning** to estimate test case volumes and hours
5. **Check 💰 Budget Planner** — labor costs auto-pull from Config; add tools and infrastructure costs
6. **View 📋 Estimation Dashboard** — all techniques aggregate here for a side-by-side comparison
7. **Use 📅 Sprint Resource Plan** to track actuals sprint by sprint

### Cell Colour Legend

| Colour | Meaning |
|--------|---------|
| 🟩 Dark Green | **User Input** — fill these cells with your data |
| 🟦 Dark Blue-Purple | **Formula** — auto-calculated, do not edit |
| 🟪 Purple/Teal header | **Section header** — labels only |

### Estimation Technique Reference

| Technique | Best Used When |
|-----------|---------------|
| **PERT** | Phases are well defined; high uncertainty exists |
| **Three-Point** | Feature list is known; range of effort is uncertain |
| **Story Points** | Agile/Scrum teams with historical velocity data |
| **Analogy** | Similar past projects exist for comparison |
| **Use Case Points** | Requirements are expressed as use cases |

> 💡 **Best Practice:** Use 2–3 techniques and compare. PERT is recommended as the primary estimate. If outcomes are within 15% of each other, confidence is high.

---

## 🎨 Design System

All dashboards share a consistent dark theme:

| Element | Hex Colour |
|---------|-----------|
| Background (dark) | `#1E1E2E` |
| Header (near-black) | `#12122A` |
| Accent — Purple | `#6C63FF` |
| Accent — Teal | `#00D4AA` |
| Accent — Red | `#FF6B6B` |
| Accent — Yellow | `#FFD93D` |
| Accent — Cyan | `#4ECDC4` |
| Accent — Orange | `#FF8C42` |
| Text (muted) | `#B0B0CC` |

---

## 🛠️ Requirements

- **Microsoft Excel 2016 or later** (recommended) — for full formula and formatting support
- **Excel 365** — for dynamic array functions where used
- Python `openpyxl` ≥ 3.1 is used to generate/maintain the `.xlsx` files programmatically

To regenerate `QA_Estimation_Template.xlsx`:

```bash
pip install openpyxl
python build_estimation_dashboard.py
```

---

## 📂 Project Structure

```
excel_tutorial/
├── README.md
├── build_estimation_dashboard.py       # Script to build QA_Estimation_Template.xlsx
│
├── Excel_Dashboard_Tutorial.xlsx       # Tutorial / reference workbook
│
├── Dashboard1_HR_Overview.xlsx         # HR: Overview & KPIs
├── Dashboard2_Salary_Analysis.xlsx     # HR: Salary analysis
├── Dashboard3_Demographics.xlsx        # HR: Workforce demographics
├── Dashboard4_JobTitle.xlsx            # HR: By job title
├── Dashboard5_Tenure.xlsx              # HR: Tenure & retention
├── Dashboard6_Employee.xlsx            # HR: Employee explorer
│
├── QA_Dashboard.xlsx                   # QA: Bug tracker & sprint health
└── QA_Estimation_Template.xlsx         # QA: Resource & budget estimation
```

---

## 📄 License

This project is provided for educational and professional use. Feel free to adapt the templates for your own projects.


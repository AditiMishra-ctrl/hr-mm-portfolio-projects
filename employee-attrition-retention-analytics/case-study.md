# Case Study — Employee Attrition & Retention Analytics
*Aditi Mishra | People Analytics, Power BI, Excel*

---

## 1. Problem Statement

**How can an organization identify which employees are most at risk of leaving — and what interventions will most effectively retain them?**

Most HR teams rely on exit interviews to understand attrition. But exit interviews are reactive — the decision to leave was made months earlier. This project takes a **predictive, data-first approach** to retention.

---

## 2. Dataset

- **Source**: IBM HR Analytics Employee Attrition Dataset (publicly available on Kaggle)
- **Records**: 1,470 employees
- **Features**: 35 variables including age, department, salary, job satisfaction, overtime, tenure, work-life balance, manager rating, and attrition status
- **Attrition Rate in Dataset**: 16.1% (237 out of 1,470 employees left)

> **[NOTE]** This is a real, publicly available HR dataset used for analytics practice. All findings are data-driven.

---

## 3. Analytical Approach

### Step 1: Data Cleaning & Exploration (Excel)
- Removed irrelevant columns (EmployeeCount, StandardHours — constant values)
- Checked for nulls and outliers
- Created attrition flag: 1 = Left, 0 = Stayed
- Calculated attrition rate by every dimension

### Step 2: Correlation Analysis
- Identified which variables have the strongest correlation with attrition
- Key finding: Overtime, Monthly Income, Job Level, and Years at Company are the top 4 predictors

### Step 3: Segmentation Analysis
- Broke down attrition rate by: Department, Job Role, Age Group, Salary Band, Tenure, Overtime Status, Work-Life Balance Score
- Identified the "highest-risk" employee profile

### Step 4: Cost of Turnover Modeling *(Assumption-labeled)*
- Calculated cost per exit: 50% of salary for junior roles, 100% for mid, 150% for senior
- Calculated total annual turnover cost by department

### Step 5: Retention Intervention Design
- Mapped top risk factors to specific, implementable HR interventions
- Prioritized by: impact (% attrition reduction) × affected population size

---

## 4. Key Findings

### Finding 1: Overtime is the #1 Attrition Driver
| Overtime Status | Attrition Rate |
|---|---|
| Works Overtime | **30.5%** |
| Does Not Work Overtime | 10.4% |

→ Employees working overtime are **3x more likely to leave**. Yet 28% of the workforce is on overtime.

### Finding 2: Salary Below Median = 2x Risk
| Salary Band | Attrition Rate |
|---|---|
| Below median (< ₹5L equiv.) | **26.3%** |
| Median to 75th percentile | 13.1% |
| Above 75th percentile | 7.2% |

→ The bottom salary quartile drives disproportionate attrition. A targeted compensation correction for high-performing bottom-quartile employees is the single highest-ROI intervention.

### Finding 3: First 2 Years Are Critical
| Tenure Band | Attrition Rate |
|---|---|
| 0–1 years | **31.4%** |
| 1–2 years | **29.8%** |
| 2–5 years | 18.6% |
| 5+ years | 11.2% |

→ Nearly 1 in 3 new joiners leaves within 2 years. Onboarding experience and early career investment are critical.

### Finding 4: Sales Roles Are the Highest-Risk Department
| Job Role | Attrition Rate |
|---|---|
| Sales Representative | **39.8%** |
| Lab Technician | 23.9% |
| Human Resources | 23.1% |
| Research Scientist | 16.1% |
| Manager | 4.9% |

### Finding 5: Work-Life Balance Score Matters
| WLB Score | Attrition Rate |
|---|---|
| 1 (Poor) | 31.3% |
| 2 | 16.7% |
| 3 | 15.7% |
| 4 (Excellent) | 17.0% |

→ Score 1 employees have 2x the attrition risk. Early identification and manager intervention can prevent exits.

---

## 5. High-Risk Employee Profile

An employee is **highest attrition risk** if they match 3+ of the following:
- ✅ Works overtime
- ✅ Salary in bottom 25% of their band
- ✅ Tenure < 2 years
- ✅ Job Role = Sales Rep or Lab Tech
- ✅ Work-Life Balance Score = 1 or 2
- ✅ No promotion in last 3 years

**Employees matching 4+ criteria**: 11% of workforce → responsible for **41% of all attrition**

---

## 6. Cost of Turnover Analysis *(Assumption-labeled)*

> **[ASSUMPTION]** Replacement cost = 75% of annual salary (industry benchmark, SHRM 2023)

| Department | Headcount | Attrition Rate | Exits/Year | Avg Salary | Cost/Exit | Total Annual Cost |
|---|---|---|---|---|---|---|
| Sales | 446 | 20.6% | 92 | ₹6.2L | ₹4.65L | ₹4.28 Cr |
| R&D | 961 | 13.8% | 133 | ₹8.1L | ₹6.08L | ₹8.09 Cr |
| HR | 63 | 19.0% | 12 | ₹5.8L | ₹4.35L | ₹0.52 Cr |
| **TOTAL** | **1,470** | **16.1%** | **237** | — | — | **₹12.89 Cr/year** |

---

## 7. Retention Interventions (Prioritized)

### Intervention 1: Overtime Management Policy
- **Target**: Employees on consistent overtime (>10 hrs/week) for 3+ months
- **Action**: Manager flag + mandatory workload review; aim to reduce overtime population by 40%
- **Projected Impact**: Reduce attrition in this segment from 30.5% to ~18% → save 30 exits/year
- **Effort**: Low (policy change, no cost)

### Intervention 2: Compensation Correction for High Performers in Bottom Quartile
- **Target**: Bottom-quartile salary employees with performance rating 3+ and tenure <2 years
- **Action**: Salary band correction during mid-year review cycle
- **Projected Impact**: Reduce attrition from 26% to ~15% in this group → save 25 exits/year
- **Effort**: Medium (budget required — estimated ₹40L incremental salary cost vs. ₹1.5 Cr saved)

### Intervention 3: Enhanced Onboarding & 90-Day Check-ins
- **Target**: All new joiners (0–6 months tenure)
- **Action**: Structured 30/60/90-day manager check-ins; buddy program; skip-level meeting at 3 months
- **Projected Impact**: Reduce Year-1 attrition from 31% to ~22% → save 15 exits/year
- **Effort**: Low (process change, no significant cost)

### Intervention 4: Sales Role Retention Program
- **Target**: Sales Representatives (39.8% attrition)
- **Action**: Career pathing clarity (Sales → Senior Sales → Sales Lead → Manager track); quarterly incentive review; manager training on recognition
- **Projected Impact**: Reduce Sales attrition from 39.8% to ~28% → save 22 exits/year
- **Effort**: Medium

---

## 8. Dashboard Design (Power BI)

**Dashboard Pages Built:**
1. **Overview**: Total headcount, attrition rate, YoY trend, attrition by gender/age/department
2. **Risk Drivers**: Waterfall chart of top 7 attrition drivers; correlation heatmap
3. **Segment Deep-Dive**: Attrition rate by job role, salary band, tenure, WLB score
4. **Cost of Turnover**: Department-wise turnover cost; monthly trend
5. **At-Risk Employees**: List view of employees matching 3+ risk criteria (for HR manager use)

---

## 9. Key Learnings

1. **Overtime is the single most actionable lever** — policy change, zero cost, high impact
2. **Early tenure is make-or-break** — invest in onboarding, not just exit interviews
3. **Data democratization matters** — HR teams need self-serve dashboards, not monthly Excel reports
4. **Attrition is a leading indicator of culture** — fix the root cause, not just the symptom

---

*See also: metrics.md, star-stories.md, resume-bullets.md*

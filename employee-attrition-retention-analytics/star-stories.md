# STAR Stories & Interview Pitches — Employee Attrition Analytics
*Aditi Mishra | HR / People Analytics Interview Prep*

---

## 30-Second Pitch

"I built a People Analytics Dashboard analyzing 1,470 employee records from the IBM HR dataset to identify the key drivers of voluntary attrition. The top finding was that employees working overtime are 3x more likely to leave — 30.5% attrition vs. 10.4% for non-overtime employees. I quantified the total annual turnover cost at ₹12.89 Cr and designed 4 targeted retention interventions projected to reduce attrition by 8–12 percentage points."

---

## 60-Second Pitch

"Most organizations manage attrition reactively — through exit interviews, after the decision to leave has already been made. I took a predictive, data-first approach.

Using the IBM HR Analytics dataset of 1,470 employees, I built an interactive Power BI dashboard that identifies the top drivers of voluntary attrition. Key findings: overtime is the #1 driver — employees working overtime have 3x the attrition risk. The first two years of tenure are critical — 31% of new joiners leave within Year 1. And Sales Representatives have the highest role-level risk at 40%.

I modeled the cost of turnover at ₹12.89 Cr annually for the organization, then designed 4 prioritized retention interventions — starting with an overtime management policy that requires zero budget but can reduce attrition by 5–8 percentage points in the affected segment.

The core insight: attrition is predictable, and the most impactful interventions are often the cheapest ones."

---

## 2-Minute Deep Dive

"Let me walk you through the Employee Attrition Analytics project.

**Why I built it**: HR teams typically find out why employees left through exit interviews — which is too late. I wanted to build a tool that lets HR identify at-risk employees before they resign, using the data organizations already have.

**The Data**: I used the IBM HR Analytics dataset — 1,470 employee records, 35 variables including compensation, tenure, overtime, work-life balance score, job satisfaction, and attrition status. 16.1% of employees in the dataset had left.

**The Analysis**: I did three things. First, correlation analysis to find which variables have the strongest relationship with attrition. Second, segmentation analysis — breaking down attrition rates by department, role, salary band, tenure, and overtime status. Third, cost modeling — translating attrition rates into rupee impact by department.

**Top Findings**:
- Overtime: 30.5% attrition for overtime employees vs. 10.4% for others — the single biggest lever
- Tenure: 31% attrition in Year 1 — onboarding quality is critical
- Sales Reps: 40% attrition — highest of any role
- Bottom salary quartile: 2.1x higher attrition risk than mid-quartile

**The Cost**: ₹12.89 Cr annual turnover cost across the organization — mostly driven by R&D and Sales volume.

**The Recommendations**: Four interventions, prioritized by impact-to-effort ratio. The overtime policy is #1 — policy change, no cost, projects to save 30 exits per year.

**The Dashboard**: Built in Power BI — 5 pages covering overview, risk drivers, segment deep-dives, cost of turnover, and an at-risk employee watchlist for HR managers."

---

## STAR Story — Data to Insight

**Situation**: I wanted to address a gap in HR decision-making — most retention strategies are intuition-based rather than data-driven. I chose to build a predictive people analytics project using a real, publicly available HR dataset.

**Task**: Analyze 1,470 employee records to identify the top drivers of voluntary attrition, quantify the business cost, and design prioritized retention interventions.

**Action**:
- Cleaned and explored 35-variable IBM HR dataset in Excel; removed noise variables, created attrition flags
- Performed correlation analysis to identify top 4 predictors: overtime, income, job level, tenure
- Segmented attrition rates across 8 dimensions; identified overtime (30.5%), new-tenure (31%), and Sales (40%) as priority segments
- Modeled annual cost of turnover at ₹12.89 Cr using SHRM benchmark (75% of salary)
- Designed 4 retention interventions with effort/impact scoring; prioritized overtime policy as #1 (zero cost, high impact)
- Built 5-page interactive Power BI dashboard for HR manager use

**Result**: A complete, data-backed people analytics report with quantified turnover cost and actionable retention roadmap — demonstrating that the 11% of employees matching 4+ risk criteria are responsible for 41% of all attrition.

---

## HR Interview Q&A

**Q: How did you decide which variables to include in your attrition analysis?**

"I started with a hypothesis-first approach: what are the known drivers of voluntary attrition from HR research? Compensation, workload (overtime), career growth, tenure, and manager relationship. I then validated each against the data — ran correlation analysis and attrition rate breakdowns for every variable. Variables with <0.05 correlation and no meaningful attrition differential (like EmployeeCount, StandardHours) were excluded. I also avoided multicollinearity — for example, Job Level and Monthly Income are highly correlated, so I prioritized Income as the cleaner signal."

**Q: What would you do differently if you had access to real company data vs. the IBM dataset?**

"Three things. First, I'd add time-series data — the IBM dataset is a snapshot; real data would let me track when attrition risk spikes (quarter-end? after performance reviews?). Second, I'd add qualitative signals — manager survey scores, Glassdoor sentiment, internal engagement survey verbatims. Third, I'd build a live early-warning system rather than a static dashboard — if an employee's overtime hours cross a threshold for 8 weeks straight, an automatic alert goes to their HR business partner. That's the difference between descriptive analytics and predictive HR."

**Q: Your analysis found overtime is the #1 driver. But what if the company genuinely needs people to work overtime?**

"Great pushback. The intervention isn't 'eliminate overtime' — it's 'manage overtime deliberately.' If overtime is structurally required, the question becomes: are we compensating for it adequately? Are we distributing it fairly or is it concentrated on the same people? Are we tracking burnout signals alongside it? I'd recommend a manager dashboard that flags when any individual has been on overtime for 8+ consecutive weeks — triggering a mandatory workload review conversation. The goal is visibility and action, not a blanket policy."

---

## Resume Bullets — HR Version

**People Analytics / HR Analytics Roles:**
- Built a 5-page interactive Power BI dashboard analyzing 1,470 employee records (IBM HR dataset) to identify key attrition drivers; found overtime (30.5% vs. 10.4% attrition) and sub-median compensation (2.1x risk) as top predictors
- Performed correlation and segmentation analysis across 35 variables; identified that 11% of employees matching 4+ risk criteria drive 41% of all voluntary attrition — enabling targeted HR intervention
- Modeled annual cost of turnover at ₹12.89 Cr using SHRM benchmark; designed 4 prioritized retention interventions with projected 8–12pp attrition reduction *(assumption-labeled)*
- Designed at-risk employee watchlist (Power BI) enabling HR managers to proactively intervene before resignation; first intervention requires zero budget (overtime management policy)

**Consulting / Business Analyst Version:**
- Applied people analytics to quantify the business cost of employee attrition (₹12.89 Cr annual) and identify the top 4 drivers across 1,470 records; used correlation analysis and segmentation to isolate highest-ROI retention interventions
- Designed an intervention prioritization matrix: overtime policy (zero cost, -5–8pp attrition), compensation correction (₹40L cost → ₹1.5 Cr saving), enhanced onboarding, and sales retention program

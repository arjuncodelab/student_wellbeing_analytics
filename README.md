## Student Wellbeing & Digital Behavior Analysis
#### Project Goal
In an era of increasing digital consumption, how does "Doom-Scrolling" affect the academic success of students globally? I designed a relational database to audit 50,000+ student records, identifying the tipping point where digital addiction leads to academic failure.

#### The Architecture
- **Normalization**: 01_schema_design.sql
Transformed a flat 'Mixed' dataset into a relational schema (Students, Countries, Academics, Mental Health, Financial Behaviour).

- **Data Integrity**: 02_data_etl.sql
Implemented strict CHECK constraints and Foreign Key relationships to ensure zero data leakage.

- **The Insights**: 03_queries_used_for_analytical_insights

#### Key Findings
- **Wellbeing Tipping Point** | _Goal_: Identify if there is a 'cliff' where internet usage destroys wellbeing.
- **Insight**: Students with 3 hours of daily internet access report the highest wellbeing scores (63.1), representing optimal digital health. However, as usage increases, wellbeing deteriorates steadily:
  
3 hours/day → Wellbeing: 63.1 

4.5 hours/day → Wellbeing: 58.88

5.5 hours/day → Wellbeing: 55.64

7 hours/day → Wellbeing: 51.38 | Critical threshold

Beyond 7 hours, students experience a 10-point wellbeing decline from the optimal range. This suggests a "danger zone" where excessive screen time becomes psychologically destructive.


- **Brain Rot Productivity Tax** | _Goal_: Do students with above-average 'Brain Rot' scores perform worse?

**Insight**: Students with above-average brain rot scores show a 12% productivity decline:
  - Below-average brain rot (11.75) :- Productivity: 9.43 
  - Above-average brain rot (26.14) :- Productivity: 8.29 

Students in the high brain rot group score up to Max of 59 out of 100, indicating severe digital addiction patterns. Even among high-attendance students (>80%), this cognitive deterioration remains consistent, suggesting brain rot is independent of effort and attendance—it's about quality of focus, not quantity of time spent.

- **Behavioral Spending & Ad Engagement** | _Goal_: Is ad clicking a stronger driver of spending than family income?

**Insight**: A student from a low-income family with high ad engagement ($35.62/month) spends more than a high-income student with low ad engagement ($53.94 is still lower than $100). More importantly, impulse scores remain consistently high (5.3-5.6) across all income levels when ad engagement is high, proving that algorithmic manipulation bypasses socioeconomic safeguards.


-** Multi-Factor Academic Risk** | _Goal_: Identify the volume of students meeting the "Triple Threat" criteria: High Late Night usage + Low attendance + High Anxiety.
- **Insight**: The high-risk group shows a 63% anxiety increase and attendance collapse of 22 percentage points. These students are experiencing a vicious cycle: late-night scrolling which leaad to disrupted sleep -> reduced class attendance -> academic anxiety -> more scrolling. Though statistically rare, they represent failures and should be flagged for early support.

|Risk Level|	Student Count| Avg Anxiety	Attendance Rate|

|High Risk|53|7.95|68.23%|

|Standard Risk|499,947|4.86|90.77%| 

- **Economic_resilience** | _Goal_: Compare how family income affects wellbeing across different country development levels.
- **Insight**:  Students in underdeveloped regions report 7-point higher wellbeing than developed nations despite lower overall infrastructure. Possible explanations:
  - Lower social media penetration = less doom-scrolling
  - Stronger community/offline activities = better mental health
  - Lower economic pressure = reduced financial anxiety
  - Reduced ad exposure = fewer impulse spending triggers
- _**Implication**_: Digital wellbeing may be inversely correlated with development level, challenging the narrative that "more technology = better outcomes."

- **Device Access Parity** | _Goal_: Measure the Academic Risk differene between students.
- **Insight**: Access paradox—giving students more devices increases risk. Shared devices create natural friction: waiting for family members, public accountability, and limited availability. This unintentionally protects users from compulsive doom-scrolling. Students with Both(smartphones + laptops) are riskier despite having better tools.

|Device Access|Avg Risk Score|Avg Productivity|

|Shared Device|0.09|8.90|

|Smartphone|0.11|8.84|

|Laptop|0.12|8.77|

|Both (Phone + Laptop)|0.13|8.74|

-**_Implication_**: Policy should consider "friction as a feature"—controlled device access may be more protective than unlimited access.


- **Digital Addiction Recovery**:- The Gold Standard Student | _Goal_: What percentage of students successfully balance high study and low social media?
- **Insight**: The 14% who achieve the "gold standard".
   - Standard student: 53.7 min/study
   - Gold standard: 56.59 min/study
   - Advantage: 2.89 additional Minutes If continued for 50 session, it become 2.4 hours extra hours. Seemingly small, but influential over an academic year.
- **_Implication_**: Small behavioral changes (reducing social media) yield measurable cognitive improvements. The 14% "recovery rate" suggests digital addiction is reversible with intentional effort.



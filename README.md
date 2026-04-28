## Student Wellbeing & Digital Behavior Analysis
#### Project Goal
In an era of increasing digital consumption, how does "Doom-Scrolling" affect the academic success of students globally? I designed a relational database to audit 50,000+ student records, identifying the tipping point where digital addiction leads to academic failure.

#### The Architecture
- Normalization: 01_schema_design.sql
Transformed a flat 'Mixed' dataset into a relational schema (Students, Countries, Academics, Mental Health, Financial Behaviour).

- Data Integrity: 02_data_etl.sql
Implemented strict CHECK constraints and Foreign Key relationships to ensure zero data leakage.

- The Insights: 03_queries_used_for_analytical_insights

###### Key Findings
- Wellbeing Tipping Point
Goal: Identify if there is a 'cliff' where internet usage destroys wellbeing.

Insight: 7 hours per day is the critical threshold where internet usage begins destroying wellbeing, while 3 hours per day shows the highest quality of wellbeing.

Quartile	Avg Wellbeing	Avg Internet Access (hours/day)
Low	63.10	3.0
Mid	58.88	4.48
High	55.64	5.55
Max	51.38	7.04

- Brain Rot Productivity Tax
Goal: Do students with above-average 'Brain Rot' scores perform worse?

Insight: Yes. Students with above-average Brain Rot (26.14) show 8.29 average productivity, while those below average (11.75) achieve 9.43 average productivity.

Brain Rot Group	Avg Productivity	Avg Brain Rot
Above Average Brain Rot	8.29	26.14
Below or Equal Avg Brain Rot	9.43	11.75

- Behavioral Spending & Ad Engagement
Goal: Is ad clicking a stronger driver of spending than family income?

Insight: High ad engagement drives higher digital spending regardless of family income level. Students with high ad engagement show significantly higher impulse purchase scores.

Family Income Level	Ad Engagement	Avg Digital Spending/Month	Avg Impulse Score
High	High	$100.07	5.63
High	Low	$53.94	2.51
Low	High	$35.62	5.34
Low	Low	$23.88	2.53

- Multi-Factor Academic Risk
Goal: Identify the volume of students meeting the "Triple Threat" criteria: High Late Night usage + Low attendance + High Anxiety.

Insight: High-risk students exhibit significantly higher anxiety (7.95 vs. 4.86), maximum late-night usage patterns, and substantially lower class attendance (68.23% vs. 90.77%).

Risk Assessment	Avg Anxiety	Avg Late Night Score	Avg Class Attendance Rate
High Risk	7.95	3.0	68.23%
Standard Risk	4.86	1.13	90.77%

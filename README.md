## Student Wellbeing & Digital Behavior Analysis
### Project Goal:
In an era of increasing digital consumption, how does "Doom-Scrolling" affect the academic success of students globally?
I designed a relational database to audit 50,000+ student records, identifying the tipping poiny ehrtr digial addiction leads to acdemic failure.

### The Architecture:
##### - Normalization: 01_schema_design.sql
Transformed a flat 'Mixed' dataset into a relational schema (Students, Countries, Academics, Mental Health, Financial Behaviour).
##### - Data Integrity: 02_data_etl.sql
Implemented strict CHECK constraints and Foreign key relationships to ensure zero data leakage.
##### - The Insights: 03_queries_used_for_analytical_insights
-- Q. Wellbeing Tipping point

Goal: Identify if there is a 'cliff' where internet usage destroys wellbeing.

Insight: 7 hours a day is the cliff where internet_usage actually destroying wellbeing while 3 hours a day internet usage show highest quality of wellbeing.

+----------+---------------+--------------------------+

| Quartile | avg_wellbeing | avg_internet_access_hour |

+----------+---------------+--------------------------+

| Max      | 51.38         | 7.04                     |

| High     | 55.64         | 5.55                     |

| Mid      | 58.88         | 4.48                     |

| Low      | 63.1          | 3.0                      |

+----------+---------------+--------------------------+


-- Q. Brain Rot Productive Tax

Goal: Do students with above average 'Brain Rot' scores actually perform worse?

Insight: Yes, above average 'Brain Rot' (26.14) have average productivity of 8.2 while students who have Brain Rot below average (11.75) have average porductivity of 9.43.
+------------------------------+------------------+---------------+

|       brain_rot_group        | avg_productivity | avg_brain_rot |

+------------------------------+------------------+---------------+

| above_avg_brain_rot          | 8.29             | 26.14         |

| below_or_equal_avg_brain_rot | 9.43             | 11.75         |

+------------------------------+------------------+---------------+


-- Q. Behavioral Spending

Goal: Is ads_clickeding a stronger driver of spending than family income?

Insight: Across Family Income level (High, Moderate, Low) shows that High ads engagment lead to high digital spending and higher impulse purchase score.

+---------------------+---------------+--------------------------------+-------------------+

| family_income_level | ad_engagement | avg_digital_spending_per_month | avg_impulse_score |

+---------------------+---------------+--------------------------------+-------------------+

| High                | High          | 100.07                         | 5.63              |

| Low                 | High          | 35.62                          | 5.34              |

| High                | Low           | 53.94                          | 2.51              |

| Low                 | Low           | 23.88                          | 2.53              |

+---------------------+---------------+--------------------------------+-------------------+


-- Q. Multi_factor Academic_risk.

Goal: Identify the volume of studnets meeting the 'Triple Threat" | Criteria: High Late Night usage, Low attendance and High Anxiety.

High Risk Students have Higher Average Late Night Score (Low = 1, Mid = 2, High = 3). Higher Anxiety Score and Lower Class Attendance.

+----------------+-------------+----------------------+---------------------------+

| Risk_assesment | avg_anxiety | avg_late_night_score | avg_class_attendance_rate |

+----------------+-------------+----------------------+---------------------------+

| High_Risk      | 7.95        | 3.0                  | 68.23                     |

| Standard_Risk  | 4.86        | 1.13                 | 90.77                     |

+----------------+-------------+----------------------+---------------------------+


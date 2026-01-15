# Case Study: Bellabeat Smart Device Usage Analysis

![R](https://img.shields.io/badge/Language-R-276DC3?logo=r)
![Tidyverse](https://img.shields.io/badge/Tidyverse-Core-C13737?logo=rstudio)
![Status](https://img.shields.io/badge/Status-Completed-success)
[![View Report](https://img.shields.io/badge/HTML-View_Report-E34F26?logo=html5&style=flat)](capstone_project.html)

## 📌 Abstract
Bellabeat, a high-tech manufacturer of health-focused products for women, seeks to become a larger player in the global smart device market. This project analyzes smart device fitness data from non-Bellabeat products (Fitbit) to identify consumer usage trends. The goal is to translate these patterns into high-level marketing strategies for the Bellabeat executive team.

The analysis focuses on the relationship between activity intensity, sedentary behavior, and caloric expenditure. The results demonstrate that while the user base is predominantly sedentary, **"Light Activity"** is the primary driver of daily step counts, suggesting a marketing pivot away from high-intensity athletics toward everyday wellness.

---

## 📂 Data & Preprocessing
The analysis utilizes the [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit) (CC0: Public Domain), sourced from Kaggle.
* **Sample:** 30 eligible Fitbit users (35 unique IDs identified during processing).
* **Timeframe:** March 2016 – May 2016.
* **Features:** Daily Steps, Calories, Distance, and Activity Intensity (Very, Fairly, Lightly, Sedentary).

### Preprocessing Pipeline
1.  **Data Integrity Check:** Verified ROCCC (Reliable, Original, Comprehensive, Current, Cited). Identified limitations regarding sample size (n=30) and lack of demographic context.
2.  **Temporal Conversion:** Converted `ActivityDate` from character string to Date objects; extracted `Day_of_Week` for behavioral analysis.
3.  **Standardization:** Utilized `janitor::clean_names()` to standardize column naming conventions for consistent analysis.

---

## 📊 Summary Statistics & User Behavior
The dataset revealed consistent behavioral patterns across the week, with no significant "slump" days, though a minor peak in activity was observed on Saturdays.

| Metric | Mean (Average) | Interpretation |
| :--- | :--- | :--- |
| **Daily Steps** | 6,547 | Moderately Active (Below the 10k benchmark) |
| **Calories Burned** | 2,189 | Consistent with average BMR + Moderate Activity |
| **Sedentary Time** | 995 mins | ~16.5 Hours/Day (High Opportunity for Intervention) |
| **Lightly Active Time** | 192 mins | Primary source of movement |
| **Very Active Time** | 21 mins | Minimal contribution to daily routine |

---

## 🔍 Key Insights & Discussion

1.  **The Sedentary Epidemic:** The vast majority of user time is spent sedentary. This suggests that marketing simply to "athletes" misses the core demographic. There is a massive opportunity to market to women looking to break sedentary cycles.
2.  **The Power of "Light" Movement:** The strong correlation between Light Activity and Total Steps suggests that users achieve their goals through accumulation of small movements, not just gym sessions.
3.  **Weekend Warriors:** Activity levels remain relatively stable but peak slightly on Saturdays, indicating users have more time or inclination for movement on weekends.

---

## 🚀 Strategic Recommendations
Based on the data, the following recommendations were presented to the Bellabeat executive team:

* **Campaign: "Step Up for Health":** Capitalize on the strong Steps/Calories correlation by gamifying daily step counts in the Bellabeat app.
* **Focus on Low-Barrier Entry:** Re-orient marketing materials to celebrate *Light Activity* (e.g., "Walking the dog counts," "Take the stairs"). This lowers the psychological barrier to entry for the predominantly sedentary user base.
* **Inactivity Alerts:** Develop a feature that triggers a "Time to Move" notification after prolonged periods of sedentary behavior, directly addressing the 16.5-hour average sedentary time.

---
*© 2025 Ryan Tang.*

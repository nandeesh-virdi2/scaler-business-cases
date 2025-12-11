---

# 🚲 **Yulu Demand Analysis & Root Cause Study**

A statistical investigation into demand fluctuations for shared electric bikes, with business insights on what drives usage patterns.

---

## 📌 **Problem Statement**

Yulu observed a noticeable decline in ride demand in recent periods.
The objective of this project is to analyze bike-sharing data and determine **which factors influence user demand**, and **identify the root causes behind periodic dips**.

---

## 📊 **Dataset Description**

The dataset contains hourly rental records including:

| Feature    | Description                       |
| ---------- | --------------------------------- |
| datetime   | timestamp of rental               |
| season     | spring / summer / fall / winter   |
| holiday    | holiday indicator                 |
| workingday | non-weekend & non-holiday         |
| weather    | categorical weather code          |
| temp       | actual temperature                |
| atemp      | perceived (feel-like) temperature |
| humidity   | humidity level                    |
| windspeed  | wind speed                        |
| casual     | number of casual riders           |
| registered | number of registered riders       |
| count      | total number of riders            |

> The `count` variable is the target for analysis.

---

## 🧠 **Key Questions Addressed**

✔ What factors drive demand for shared bikes?
✔ Does seasonality explain dips in user count?
✔ Do weather conditions impact rental behaviour?
✔ Do holidays or working days influence usage?
✔ Is there statistical evidence supporting these effects?

---

## 🔍 **Approach & Methodology**

1. **Data Cleaning & Feature Engineering**

   * Conversion of datetime into year, month, day, hour.

2. **Exploratory Data Analysis**

   * Distribution checks
   * Seasonal and hourly trends
   * Scatter plots vs environmental variables
   * Correlation study

3. **Hypothesis Testing**

   * Independent t-tests (working day & holiday effects)
   * Shapiro & Levene tests for assumptions
   * Kruskal-Wallis non-parametric tests (weather and season effects)
   * Chi-square test (association between weather and season)

4. **Statistical Interpretation & Business Conclusions**

---

## 📈 **Key Insights**

✔ **Demand rises from 2011 to 2012**, reflecting growth in adoption.
✔ **Strong hourly patterns** — peaks at 8 AM and 5–6 PM indicate commuter-centric usage.
✔ **Environmental conditions matter:**

* Temperature → *positive influence*
* Humidity → *slightly negative influence*
* Wind speed → *negative influence*

✔ **Weather & season significantly influence user demand:**

* Kruskal–Wallis tests returned extremely small p-values
* Seasonality matches monthly dips in demand

✔ **Holidays and working days are NOT statistically significant drivers**, meaning calendar-type effects are weak.

---

## 📝 **Root Cause Conclusion**

> The observed decline in demand aligns with **seasonality and adverse weather conditions**, not with calendar events like working/non-working days.

Demand dips reflect **season-driven behavioural change**, particularly during months with extreme weather.

---

## 💡 **Business Recommendations**

📍 Adjust fleet deployment seasonally
📍 Provide weather-based pricing & offers
📍 Enhance availability during commuter peak hours
📍 Improve app notifications & weather safety guidance

---

## 🔧 **Tech Stack**

* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* SciPy

---
**🔗 **Author****

Nandeesh Virdi

Email: nandeesh.virdi2@gmail.com

LinkedIn: www.linkedin.com/in/nandeesh-virdi-930331159

---


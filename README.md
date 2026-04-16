# chicago-taxi-analysis
## Problem
Exploratory Data Analysis (EDA) and hypothesis testing on Chicago taxi trips to analyze the impact of weather on ride frequency.
## 🛠️ What I Did (Step-by-Step)

### 1. Data Acquisition & Web Scraping
* **Process:** Developed a script to extract historical weather data for Chicago (November 2017) from an external web source.
* **Goal:** Create a baseline of environmental conditions to correlate with trip performance.

### 2. Exploratory Data Analysis (SQL)
* **Action:** Queried the primary database to identify trip volumes per company between November 15-16, 2017.
* **Result:** Ranked companies by `trips_amount` to understand the competitive landscape and market share.

### 3. Deep Dive & Storytelling (Python)
* **Analysis:** Cleaned and processed datasets containing taxi companies and drop-off neighborhoods.
* **Insights:** * Identified the **Top 10 neighborhoods** by drop-off frequency.
    * Utilized visualizations (**Seaborn/Matplotlib**) to perform storytelling, identifying the "Loop" and "O'Hare" as critical strategic zones.
### 📊 Top Neighborhoods by Drop-offs
Through data aggregation, I identified the strategic hubs where Zuber should focus its initial fleet deployment:

| Neighborhood | Drop-off Frequency | Strategic Importance |
| :--- | :--- | :--- |
| **Loop** | High | Business & Financial Hub |
| **River North** | High | Entertainment & Tourism |
| **Streeterville** | Medium-High | Residential & Commercial |
| **West Loop** | Medium | Tech & Gastronomic District |
| **O'Hare** | Critical | Primary International Gateway |

> **Operational Note:** Focusing operations in these top 5 areas covers over 60% of the total market demand identified in the EDA.

### 4. Statistical Hypothesis Testing
* **The Challenge:** Does rain actually change the duration of trips from the Loop to O'Hare International Airport on Saturdays?
* **Methodology:** * Compared two distinct populations: **Rainy Saturdays** vs. **Clear Saturdays**.
    * **Variable:** Trip duration in seconds (Quantitative).
    * **Significance Level:** $\alpha = 0.05$
* **Statistical Evidence:** The resulting **p-value** was significantly lower than alpha ($p < 0.05$).

---

## 🏆 Key Results & Learning
* **Decision:** We rejected the Null Hypothesis ($H_0$) and accepted the **Alternative Hypothesis ($H_a$)**.
* **Impact:** There is a **statistically significant difference** in trip duration during rainy Saturdays.
* **Business Application:** For an Operations Manager, this data justifies the implementation of **Dynamic Pricing** and the adjustment of **ETA (Estimated Time of Arrival)** algorithms during bad weather to maintain customer satisfaction and driver efficiency.

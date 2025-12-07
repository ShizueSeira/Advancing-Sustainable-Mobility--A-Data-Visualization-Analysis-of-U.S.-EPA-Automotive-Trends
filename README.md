# Advancing Sustainable Mobility: A Data Visualization Analysis of U.S. EPA Automotive Trends

**Team Tres Sigmas** | **Course:** 4CSE (Computer Science) | **Subject:** DataViz-E 1

---

## 👥 Team Members
* **Inventado, Charles Fredric G.**
* **Rodelas, John Vincent B.**
* **Valles, James Vincent V.**

---

## 📖 Project Overview

The project explores historical trends in the U.S. automotive industry (1975–2024) using data from the **U.S. Environmental Protection Agency (EPA)**. By utilizing advanced data visualization techniques, we analyze the progression of fuel economy, CO2 emissions, and the adoption of cleaner vehicle technologies.

### 🎯 Objectives & SDG Alignment
The analysis aims to address specific policy questions aligned with the **United Nations Sustainable Development Goals**:
* **SDG 7 (Affordable and Clean Energy):** Examining real-world fuel economy improvements and the shift toward alternative fuel vehicles.
* **SDG 13 (Climate Action):** Analyzing carbon dioxide CO2 emission reductions and the impact of vehicle weight/horsepower trade-offs on environmental goals.

---

## 📂 Repository Structure

The project follows a linear data pipeline structure:

```text
📦 Advancing-Sustainable-Mobility
 ┣ 📂 Datasets
 ┃ ┣ 📜 A-Detailed-Real-World-Fuel-Economy-Raw-Dataset.csv       # [SOURCE] Original Raw EPA Data
 ┃ ┣ 📜 Output - TresSigmas - DataCleaning.csv                   # [OUTPUT 1] Cleaned Data (0 Imputation)
 ┃ ┣ 📜 Output_TresSigmas_Rev2_CSV.csv                           # [OUTPUT 2] Cleaned Data (Revised)
 ┃ ┗ 📜 TresSigmas_DataClean_HuliNa.csv                          # [OUTPUT 3] Final Cleaned Data (Avg Imputation)
 ┃
 ┣ 📂 Visualizations
 ┃ ┣ 📜 TresSigmas_Proposal_Visualization_v1.twb                 # Tableau Dashboard (Baseline Analysis)
 ┃ ┣ 📜 TresSigmas_Proposal_Visualization_v2.twb                 # Tableau Dashboard (Refined Analysis)
 ┃ ┣ 📜 TresSigmas_Proposal_Visualization_v1.ipynb               # Python Analysis (Baseline Code)
 ┃ ┗ 📜 TresSigmas_Proposal_Visualization_v2.ipynb               # Python Analysis (Refined Code)
 ┃
 ┣ 📜 DataCleaning - TresSigmas.tfl                              # [PIPELINE] Tableau Prep Builder Flow
 ┗ 📜 TresSigmas_4CSE_DataViz-E 1_CourseProjectProposal_Final.pdf # Project Proposal & Literature Review
````

-----

## 📊 Methodology & Execution Workflow

Our methodology consists of two distinct phases: **Data Cleaning** and **Imputation Strategy**. The setup instructions below mirror this workflow.

### Phase 1: Data Cleaning (ETL)

  * **Tool Used:** Tableau Prep Builder (`DataCleaning - TresSigmas.tfl`)
  * **Process:**
    1.  Ingestion of `A-Detailed-Real-World-Fuel-Economy-Raw-Dataset.csv`.
    2.  Standardization of string formats (e.g., manufacturer names).
    3.  Handling of null values (see Phase 2).

### Phase 2: Imputation & Visualization Strategy

We utilized two different analytical approaches to handle missing performance data (e.g., missing specific metrics for older car models).

| Version | Methodology | Dataset Used | Purpose |
| :--- | :--- | :--- | :--- |
| **V1 (Baseline)** | **Zero (0) Imputation:** Missing numerical values replaced with 0. | `Output - TresSigmas - DataCleaning.csv` | Initial Exploratory Data Analysis (EDA) and distribution checks. |
| **V2 (Refined)** | **Average Imputation:** Missing values replaced with column/category averages. | `TresSigmas_DataClean_HuliNa.csv` | Statistical analysis minimizing skew; used for Heatmaps, Treemaps, and Dual Axis charts. |

-----

## 🛠️ Setup Instructions

Follow these steps to reproduce the analysis in the correct methodological order.

### Prerequisites

  * **Tableau Prep Builder** (for the ETL pipeline)
  * **Tableau Desktop** (for Dashboards)
  * **Python 3.x** with Jupyter Notebook (Optional, for `.ipynb` analysis)
      * *Libraries:* `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`

### Step-by-Step Execution

#### 1\. Run the Data Cleaning Pipeline

To see how the raw data was processed:

1.  Open **Tableau Prep Builder**.
2.  Load the file `DataCleaning - TresSigmas.tfl`.
3.  **Note:** If the file shows a connection error, right-click the "Input" node and locate `Datasets/A-Detailed-Real-World-Fuel-Economy-Raw-Dataset.csv` on your local machine.
4.  Run the flow to generate the output CSVs (optional, as they are already provided in the `Datasets` folder).

#### 2\. Launch the Visualizations

To view the final dashboards:

  * **For Baseline Analysis (V1):**

    1.  Open `Visualizations/TresSigmas_Proposal_Visualization_v1.twb` in Tableau Desktop.
    2.  If prompted for a data source, connect to `Datasets/Output - TresSigmas - DataCleaning.csv`.

  * **For Refined Analysis (V2 - Recommended):**

    1.  Open `Visualizations/TresSigmas_Proposal_Visualization_v2.twb` in Tableau Desktop.
    2.  If prompted for a data source, connect to `Datasets/TresSigmas_DataClean_HuliNa.csv`.
    3.  *Key Charts to Observe:*
          * **Treemap:** Manufacturer CO2 Intensity.
          * **Stacked Area:** Technology Adoption Rates.
          * **Dual Axis:** Weight vs. MPG Trends.

#### 3\. (Optional) Run Python Analysis

1.  Navigate to the `Visualizations` folder.
2.  Open `TresSigmas_Proposal_Visualization_v2.ipynb` in Jupyter Notebook.
3.  Run all cells to generate the correlation heatmaps and statistical summaries.



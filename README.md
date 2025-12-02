# MinnesotaFishing

This repository contains an exploratory data analysis (EDA) of Minnesota lake fishing activity, focusing on how **temperature**, **depth**, **species**, and **lake characteristics** influence **catch counts**.  
It includes visualizations, aggregated statistics, and interactive Bokeh dashboards.

---

## Repository Structure

- `data/`  
  - `fish_data.csv` – raw input dataset

- `notebooks/`  
  - `OmniaFishling.ipynb` – main exploratory analysis

- `visuals/`  
  Static PNG plots including:  
  - temperature vs catch  
  - depth vs catch  
  - temperature vs depth  
  - species counts per lake  
  - monthly catch by lake  
  - monthly catch by species  

- `interactive/`  
  Bokeh HTML dashboards:  
  - temperature vs catch (lake dropdown + species toggle + regression)  
  - depth vs catch (lake dropdown + species toggle + regression)  
  - monthly catch trends (lake dropdown + species series)

- `README.md`

---

## Project Objective

The goal of this project is to:

- Analyze fish catch patterns across Minnesota lakes  
- Examine how environmental factors (temperature, depth) relate to catch success  
- Explore species-level behavioral differences  
- Understand seasonal patterns in fish catches  
- Build **interactive tools** to explore lake × species relationships  

This analysis is particularly relevant for ecological insights, angler decision-making, and future predictive modeling.

---

## Key Analyses & Visualizations

### **1. Data Cleaning & Quality Checks**

- Handled missing values  
- Removed duplicates  
- Converted date formats  
- Extracted `month` and `month_year` features  
- Generated summary statistics  
- Grouped summaries by lakes and species  

---

### **2. Exploratory Visualizations**

#### **Temperature vs Catch Count**
- Scatterplots per species  
- Regression lines  
- **Finding:** Temperature has a very weak correlation with catch count  

#### **Depth vs Catch Count**
- Strong depth clustering by species  
- **Conclusion:** Depth is a strong predictor of fish behavior  

#### **Temperature vs Depth**
- Correlation ≈ **0.015**  
- **Conclusion:** Temperature and depth have almost no linear relationship  

#### **Species Distribution by Lake**
- Bar chart of species × lake counts  
- **Finding:** Species composition varies widely across lakes  

#### **Catch Time Series**
- Daily & monthly trends per lake  
- Daily & monthly trends per species  
- Rolling averages  
- **Conclusion:** Catch counts exhibit seasonal patterns  

#### **Temperature Time Series**
- Average lake temperature trends by month  
- Displays strong seasonal variation  

---

## Interactive Dashboards (Bokeh)

Interactive HTML visualizations include:

- Temperature vs Catch Count  
- Depth vs Catch Count  
- Monthly Catch Count by Species  

### Features:

- Lake dropdown filter  
- Species toggle (click-to-hide)  
- Dynamic regression line updates  
- Interactive point filtering  

These enable real-time exploration of species behavior and lake-specific conditions.

---

## Conclusions

- **Depth is a stronger predictor of catch behavior than temperature**  
- **Temperature does not show a strong linear relationship with catch count**  
- **Fish species show distinct depth and habitat preferences**  
- **Catch counts follow clear seasonal patterns across months**  
- **Lakes differ significantly in species composition and total catches**  
- **Interactive filters confirm strong lake × species interactions**  

---

## Technologies Used

- Python 3  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Bokeh  
- Jupyter Notebook  

---

## How to Run

Clone the repository:

```bash
git clone https://github.com/sskr-sadu/MinnesotaFishing.git
cd MinnesotaFishing
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch the notebook:

```bash
jupyter notebook notebooks/OmniaFishling.ipynb
```

Open any HTML file in the `/interactive/` folder to explore the dashboards.

---

## Acknowledgements

This project explores Minnesota fishing data with applications in environmental science, fishery analytics, and angler decision support systems.

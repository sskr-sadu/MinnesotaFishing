# MinnesotaFishing

This repository contains an exploratory data analysis (EDA) of Minnesota lake fishing activity, focusing on how temperature, depth, species, and lake characteristics influence catch counts.
It includes visualizations, aggregated statistics, and interactive Bokeh dashboards.

## 📁 Repository Structure

- [`data/`](data/)
  - `fish_data.csv` – raw input dataset
- [`notebooks/`](notebooks/)
  - [`OmniaFishling.ipynb`](notebooks/OmniaFishling.ipynb) – main exploratory analysis
- [`visuals/`](visuals/)
  -Static PNG plots:
    - temperature vs catch
    - depth vs catch
    - temperature vs depth
    - species counts per lake
    - monthly catch by lake
    - monthly catch by species
- [`interactive/`](interactive/)
  - Bokeh HTML dashboards:
    - temperature vs catch (lake dropdown + species toggle + regression)
    - depth vs catch (lake dropdown + species toggle + regression)
    - monthly catch trends (lake dropdown + species series)
- [`README.md`](README.md)




##Project Objective
The goal of this project is to:
Analyze fish catch patterns across Minnesota lakes
Examine how environmental factors (temperature, depth) relate to catch success
Explore species-level behavior
Understand seasonality of catch activity
Build interactive tools to explore lake × species patterns
This analysis is particularly relevant for ecological insights, angler recommendations, and future predictive modeling.

##Key Analyses & Visualizations
1. Data Cleaning & Quality Checks
Handled missing values
Removed duplicates
Converted date formats
Extracted month–year features
Summary statistics for numerical fields
Grouped summaries for lakes and species
2. Exploratory Visualizations
Temperature vs Catch Count
Scatterplots per species
Regression lines
Finding: Very weak correlation
Depth vs Catch Count
Clear depth clusters by species
Conclusion: Depth influences catch strongly
Temperature vs Depth
Correlation ≈ 0.015
Conclusion: Almost no linear relationship
Species Distribution by Lake
Bar chart of species × lake counts
Finding: Species vary heavily across lakes
Catch Time Series
Daily & monthly trends per lake
Daily & monthly trends per species
Rolling averages
Conclusion: Seasonal catch patterns exist
Temperature Time Series
Average temperature trends per lake
Strong seasonal signatures

##Interactive Dashboards (Bokeh)
Interactive HTML visualizations include:
Temperature vs Catch Count
Depth vs Catch Count
Monthly Catch Count by Species
Features:
Lake dropdown filter
Species toggle
Auto-updating regression lines
Dynamic point filtering
These allow interactive exploration of lake–species behavior.

##Conclusions
Depth is a stronger predictor of catch behavior than temperature.
Temperature shows no strong linear relationship with catch.
Fish species show distinct depth and distribution patterns.
Catch counts follow clear seasonal patterns across months.
Lakes differ significantly in species composition and catch totals.
Interactive filters confirm strong lake × species interactions.

##Technologies Used
Python 3
Pandas
NumPy
Matplotlib
Seaborn
Bokeh
Jupyter Notebook

##How to Run
Clone the repository:
git clone https://github.com/sskr-sadu/MinnesotaFishing.git
cd MinnesotaFishing
Install dependencies:
pip install -r requirements.txt
Launch the notebook:
jupyter notebook notebooks/OmniaFishling.ipynb
Open any interactive HTML file in /interactive/ to explore dashboards.

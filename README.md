# ⚡ Modeling Electricity Generation in the United States

## 📌 Team Members
- Spencer Doyle  
- Abbie Kinaro  
- Ming Xia  

## 📊 Data Sources
This project utilizes electricity generation data from the **United States Energy Information Administration (EIA)**. The dataset categorizes electricity generation by sources, including:
- Coal
- Natural gas
- Nuclear electric power
- Solar
- Wind
- Hydropower
- Wood
- Petroleum

The dataset is available in **monthly records (since 1973)** and **yearly records (since 1949)**. Missing data points are marked as "Not Available," which have been processed appropriately for analysis.

## 🔍 Predictors
To analyze electricity generation trends, we incorporate key predictive factors:

**For Total Grid Size:**
- US population
- Median household income (inflation-adjusted)
- Electric car market size

**For Source-Specific Generation:**
- **Solar/Wind/Hydro**: Li-ion battery cost & market size
- **Solar**: Photovoltaic cost (residential & utility)
- **Natural Gas**: Natural gas cost
- **Coal**: Coal cost
- **Petroleum**: Oil cost

These predictors are selected based on their expected impact on electricity generation trends.

## 🔧 Data Cleaning
- **Handling Missing Data**: Replaced "Not Available" values with `NaN`, later filled with `0` when the source generation was negligible.
- **Time Granularity Decision**: While the **monthly dataset** provides more data points, it introduces noise. Since several predictors have **yearly values**, we are modeling at a **monthly level** for robustness while staying adaptable based on model performance.

## 📈 Methodology
- Data processing and integration of economic, technological, and demographic predictors.
- Regression modeling and statistical analysis to assess trends and forecast electricity generation.
- Iterative refinement of models to optimize predictions.

## 🎯 Goals
- Understand the impact of economic and technological factors on electricity generation.
- Develop predictive models for electricity generation across different sources.
- Provide insights into the future dynamics of the U.S. energy grid.

## 💬 Contributions
Contributions are welcome! If you're interested in collaborating, please reach out to the team.

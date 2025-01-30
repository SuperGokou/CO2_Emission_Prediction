Modeling Electricity Generation in the United States

Members: Spencer Doyle, Abbie Kinaro
Data Sources:
For our analysis, we are utilizing electricity generation data obtained from the United
States Energy Information Administration (EIA). The response variable in our dataset is clean
and organized, categorized by generation sources, including coal, natural gas, nuclear electric
power, solar, wind, hydropower, wood, petroleum, and others. The data is segmented monthly,
starting from 1973, though not all sources have data spanning this entire period. Instances, where
data is unavailable or missing are marked as "Not Available". For yearly analysis, the dataset
extends back to 1949, but similar to the monthly data, not all sources have data going back that
far. We have implemented data processing techniques, including handling missing values, as part
of our preparation process.
Our focus is narrowed down to eight significant sources of electricity generation: coal,
natural gas, nuclear electric power, solar, wind, hydropower, wood, and petroleum. These
sources collectively account for a significant portion of electricity generation over the years, each
contributing at least a few percent of the total electricity generation during specific periods.
Predictors:
In our predictive analysis, we are selecting specific predictors that hold significant predictive
power for both source-specific generation and overall grid generation.

For total grid size, we are considering:
● US population
● Median household income, inflation-adjusted
● Electric car market
For source-specific generation, our predictors include:
● Li-ion battery cost and market size (solar/wind/hydro)
● Photovoltaic cost, both residential and utility (solar)
● Natural gas cost (natural gas)
● Coal cost (coal)
● Oil cost (petroleum)
These predictors were chosen based on their relevance and expected impact on the respective
sources of electricity and grid size. We will employ these predictors to build predictive models
and gain insights into the dynamics of electricity generation across different sources and the
overall grid. So far, we have been able to find data and create plots for the bolded predictors, as
shown below.

Data Cleaning
In preparing our data for analysis, we first dealt with the response variable. We initiated
the cleaning process by replacing occurrences of the string “Not Available” with NaN values.
This was to facilitate easier data processing and manipulation. Upon visualizing the data and
identifying the NaN values, it became apparent that all missing data points corresponded to
source generation that was either zero or negligible in scale. To maintain data completeness, we
decided to replace these NaN values with zeros. This approach ensures that our dataset
accurately represents the absence of generation for these specific instances, allowing for a more
comprehensive analysis.
Next, we faced a decision between modeling the data on a monthly or yearly basis. The
monthly dataset offers a larger volume of data for training and testing. However, this larger
dataset might introduce additional noise, potentially leading to overfitting and poor
generalization. Moreover, several of our predictors are represented as yearly values. Attempting
to extrapolate these yearly values to a monthly scale by assuming linear changes introduces a
level of assumed linearity on an annual scale, which may not align with the actual patterns in the
monthly response data.

Despite these challenges, we are inclined to model the data monthly due to the larger
dataset size. This approach provides a more robust foundation for our analysis. If, during our
regression attempts, we encounter evident issues related to noise or overfitting, we remain open
to transitioning to the yearly data. Flexibility in our approach allows us to adapt our modeling
strategy based on the observed behavior of the models and the quality of the predictions. This
iterative process ensures that our analysis is thorough and adaptable, allowing us to draw
meaningful insights from the data.

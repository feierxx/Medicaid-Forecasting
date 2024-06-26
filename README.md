# Medicaid-Forecasting
————EMRTS project

This project is designed to forecast Medicaid enrollment and expenditure for the next decade, both nationwide and specifically for Illinois. The forecasts will be conducted using comprehensive data analyses, and the final outcomes will be presented in a visualization dashboard to facilitate clear and effective data interpretation.

## Outcome
### Script:
The analysis and forecasting code for Medicaid Expenditure and Enrollment are uploaded as expenditure.ipynb and enrollment.ipynb respectively.

[enrollment.ipynb](enrollment.ipynb): Forecasting the number of Medicaid enrollment. It follows the process of loading and cleaing the [raw data](statistic_id245347_total-medicaid-enrollment-1966-2022.xlsx) for the national enrollment, trancating the data, fitting the prophet model, and making 10-year prediction. Then it moves on to the IL state enrollemnt prediction with the same steps with the [state data](IL_enrollment.csv).

[expenditure.ipynb](expenditure.ipynb): The process is the same as enrollment forecasting process. The data used for national forecasting is [medicaid_spending_usafacts.csv](medicaid_spending_usafacts.csv) while the state data is the excel files uploaded with the format "fy20xx-statistical-chart.xlsx".

[enrollment_modeltrials.ipynb](enrollment_modeltrials.ipynb) and [expenditure_modeltrials.ipynb](expenditure_modeltrials.ipynb): These two files contains the process of additional trials of time series model, including Holt-Winter Exponential Average and ARIMA models. It starts with data processing and splitting, then move on to exploratory data analysis, multiple model training, model evaluation and final forecasting visualization. The data used in this two scripts are the same as previous.


### Visualization Dashboard

**Expenditure Dashborad:** https://mmiscloud.us/s/@feierx/expenditure-layout/

**Enrollment Dashboard:** https://mmiscloud.us/s/@feierx/medicaid-enrollment-layout/

## Data Source
### Medicaid Expenditure
**State-wise Expenditure**

State-wise expenditure data is sourced from the U.S. Department of Health and Human Services to ensure reliability ([MFCU](https://oig.hhs.gov/fraud/medicaid-fraud-control-units-mfcu/)). This data, available in the Expenditure & Statistics section, covers expenditures from all 50 states starting from 2010. It is primarily used for expenditure forecasting in Illinois and for visualization analysis. The cleansed data has already been uploaded [cleanead expenditure data by state](by_state.csv).

**Total Expenditure** 

For enhanced prediction accuracy through a longer time series, consider using the data from [USA Facts](https://usafacts.org/data/topics/people-society/poverty/poverty-programs/medicaid-spending/) for total expenditure forecasting. The reliability of this data has been confirmed by comparing it with government statistical results, ensuring its credibility for detailed analyses.

### Medicaid Enrollment
The data source for enrollment analysis is derived from two key resources: state-wise data from a government source at [Medicaid.gov](https://data.medicaid.gov/dataset/6165f45b-ca93-5bb5-9d06-db29c692a360/data) and comprehensive historical data on total enrollment from 1966 available at [Statista](https://www.statista.com/statistics/245347/total-medicaid-enrollment-since-1966/). The reliability of these sources has been verified by comparing the data with government statistical results.

## Methodology
### Language
**Python:** Use Python and Anaconda for data cleaning, analysis and forecasting. Version 3.11.5

### Pacakges
**Prophet:** Prophet is an open-source forecasting tool developed by Facebook with four main components: trend, seasonality, holidays, and an error term. It works well with data that has missing values or outliers and can incorporate trends, seasonality, and holiday effects. Available in both Python and R. Make sure the package has been downloaded before running the code by running `!pip install prophet`.

**Pandas:** Pandas is utilized for data analysis.

### Visualization tools
**Instedaq:** Instedaq is a versatile visualization tool designed to help users from various fields such as data analysis, science, and business effectively interpret and present complex data sets. It offers a user-friendly interface with options for creating dynamic visualizations like charts, graphs, and maps, tailored to specific data needs.

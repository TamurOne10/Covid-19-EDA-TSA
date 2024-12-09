# COVID-19 Dataset Forecasting Model
Overview
This repository provides an exploratory data analysis (EDA) and a forecasting model for COVID-19 cases in Pakistan. Using Python, the dataset is analyzed for patterns, cleaned for consistency, and visualized for better understanding. A predictive model is then developed using Prophet to forecast active cases.

Dataset Description
The dataset includes COVID-19 statistics from 26th February 2020 to 10th May 2020. It contains the following columns:

Date: The date of the record.
Cases: Number of confirmed cases reported on that date.
Deaths: Number of deaths reported on that date.
Recovered: Number of recovered cases reported on that date.
Travel_history: Source of infection (e.g., local contact or international travel).
Province: Province where cases were reported.
City: City where cases were reported.
Exploratory Data Analysis (EDA)
Data Cleaning:

Removed duplicates.
Corrected inconsistent city names (e.g., "ISlamabad" to "Islamabad").
Checked for missing values (no null values were found).
Data Statistics:

Basic descriptive statistics (mean, standard deviation, etc.).
Identification of unique values in columns.
Data type inspection to separate numerical and categorical variables.
Visualizations:

Pair plots to visualize relationships between numerical variables.
Bar charts to analyze deaths and cases across provinces.
Line plots to show trends in daily cases, recoveries, and deaths.
Active Case Calculation
Active cases are derived using the formula:
Active Cases = Cases - Recovered - Deaths

Forecasting Model
The forecasting model uses the Prophet library to predict active cases for the next 30 days.

Steps:
The dataset is prepared by grouping and summing active cases by date.
A Prophet model is trained on the data to predict future trends.
Predictions are visualized using interactive plots.
Requirements
Install the required Python libraries using:

bash
Copy code
pip install pandas numpy matplotlib seaborn plotly prophet
How to Use
Clone this repository:
bash
Copy code
git clone https://github.com/your-repo/covid-forecasting.git
Load the dataset: Ensure covid19_Pakistan.csv is in the working directory.
Run the Jupyter Notebook or Python script to perform EDA and generate forecasts.
Key Insights
Trends:

Active cases peaked during specific intervals.
Recovered cases increased steadily, reflecting improving health outcomes.
Regional Analysis:

Most cases were concentrated in provinces like Sindh and Punjab.
Major cities like Karachi and Lahore reported the highest cases.
Forecasting:

The Prophet model provides an estimate of active cases for decision-making.
Visualizations
Example Plots
Daily Trends:
Line plot showcasing new cases, recoveries, and deaths per day.
Bar Charts:
Number of cases and deaths per province categorized by travel history.
Future Work
Incorporate additional features like vaccination data.
Extend the forecasting model to other countries' data.
Utilize advanced machine learning models for better predictions.
Contributing
Feel free to fork this repository, make changes, and submit a pull request. Suggestions and feedback are welcome!

License
This project is licensed under the MIT License. See LICENSE for details.

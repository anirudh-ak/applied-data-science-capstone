# SpaceX Falcon 9 Launch Prediction

## Project Overview

This project aims to predict the success of SpaceX Falcon 9 first-stage landings. SpaceX can significantly reduce launch costs by reusing the first stage of its rockets. Predicting the landing success helps estimate the cost of a launch and provides insights for potential competitors.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Collection](#data-collection)
- [Data Wrangling](#data-wrangling)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Geospatial Visualization](#geospatial-visualization)
- [Interactive Dashboard](#interactive-dashboard)
- [Predictive Analytics](#predictive-analytics)
- [Results Summary](#results-summary)
- [Contributors](#contributors)

## Data Collection

### SpaceX API
- Collected launch data using the SpaceX REST API.
- Target API endpoint: `https://api.spacexdata.com/v4/launches`
- Key steps included:
  - Sending GET requests to the API.
  - Parsing JSON responses.
  - Filtering the dataset to retain only Falcon 9 launches.
  - Handling missing values and applying one-hot encoding.

### Web Scraping
- Collected additional launch data from Wikipedia.
- Target URL: `https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches`
- Key steps included:
  - Fetching HTML content using `requests.get(url)`.
  - Parsing HTML content with BeautifulSoup.
  - Extracting relevant data and converting it to a DataFrame.
  - Cleaning the data and handling missing values.

## Data Wrangling
- Loaded the cleaned data into a Pandas DataFrame.
- Performed data cleaning, including handling missing values.
- Conducted feature engineering to create new columns.
- Encoded landing outcomes into binary values.
- Exported the cleaned data to a CSV file.

## Exploratory Data Analysis
- Conducted initial exploration of the dataset.
- Visualized various aspects of the data to identify trends and patterns.

### Key Insights:
- Launch success has improved over time.
- KSC LC-39A has the highest success rate among launch sites.
- Orbits ES-L1, GEO, HEO, and SSO have a 100% success rate.
- Higher payload mass generally correlates with higher success rates.

## Geospatial Visualization
- Created geospatial visualizations using Folium.
- Key steps included:
  - Setting up a Folium map centered around launch sites.
  - Adding markers for each launch site.
  - Visualizing launch outcomes with circles.
  - Displaying launch paths with lines.
  - Saving the Folium map as an HTML file.

## Interactive Dashboard
- Built an interactive dashboard using Plotly Dash.
- Key components included:
  - Dropdown menus for selecting launch sites.
  - Pie charts and scatter plots for visualizing launch success.
  - Callback functions to update graphs based on user input.
  - Running the Dash app to display the dashboard.

## Predictive Analytics
- Developed models to predict landing outcomes.
- Key steps included:
  - Splitting data into training and testing sets.
  - Building classification models (Logistic Regression, SVM, Decision Tree, KNN).
  - Evaluating model performance using accuracy, precision, and recall.
  - Tuning hyperparameters to optimize model performance.
  - Selecting the best-performing model.
  - Saving the model for deployment.

## Results Summary

### Model Performance
- All the models performed similarly on the train and test set with the decision tree performing slightly better on the training set and slightly worse on the test set.

### Launch Sites
- **Equator:** Launch sites are predominantly located near the equator, leveraging Earth's rotational speed for a natural propulsion boost, thereby reducing the need for extra fuel and boosters.
- **Coast:** All launch sites are situated along the coast.
- **KSC LC-39A:** KSC LC-39A boasts the highest success rate among all launch sites, achieving a 100% success rate for payloads under 5,500 kg.

### Launch Success Trends
- Launch success rates have improved consistently over time.

### Orbits
- **High Success Orbits:** Orbits such as ES-L1, GEO, HEO, and SSO have maintained a 100% success rate.

### Payload Mass
- **Correlation with Success:** Generally, across all launch sites, an increase in payload mass correlates with a higher success rate.

## Contributors
- [Your Name](https://github.com/yourgithubusername)

Feel free to reach out for any questions or collaborations!

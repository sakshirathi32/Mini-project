# World War II Bombing Operations & Weather Analysis (Python Project)

## Project Overview

This project analyzes **World War II bombing operations** and compares them with **historical weather data** to study how weather conditions may have influenced bombing missions.

The project uses:

* Bombing operations dataset (missions, aircraft, target countries, locations)
* Weather station dataset (station locations and temperature records)

The main goal is to:

1. Clean and preprocess the datasets
2. Visualize bombing patterns across countries
3. Analyze weather station temperature trends
4. Compare bombing dates with temperature conditions
5. Perform **time series forecasting using ARIMA** on weather data

---

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Plotly
* Statsmodels
* Scikit-learn
* Kaggle Dataset

---

## Datasets Used

### 1. World War II Operations Dataset

Contains:

* Mission Date
* Country
* Target Country
* Aircraft Series
* Takeoff Location
* Target Location
* Latitude and Longitude
* Theater of Operations

### 2. Weather Dataset

Contains:

* Weather station locations
* Station ID
* Date
* Mean Temperature

---

## Major Functions / Methods Used

## Data Loading

### `pd.read_csv()`

Used to load CSV files into DataFrames.

**Use case:**
Reading bombing operations and weather datasets.

---

## Data Cleaning

### `pd.isna()`

Checks missing values.

**Use case:**
Removing rows where country or coordinates are missing.

### `drop()`

Removes unnecessary columns.

**Use case:**
Dropping unused features to simplify analysis.

### `loc[]`

Selects required columns.

**Use case:**
Keeping only important weather columns like temperature and date.

---

## Data Exploration

### `value_counts()`

Counts frequency of values.

**Use case:**
Finding top countries and aircraft series.

### `info()`

Shows dataset structure.

**Use case:**
Checking column types and null values.

### `head()`

Displays first few rows.

**Use case:**
Quick preview of data.

---

## Visualization

### `sns.countplot()`

Creates count-based bar charts.

**Use case:**
Visualizing country-wise bombing frequency.

### `plt.plot()`

Creates line graphs.

**Use case:**
Plotting temperature trends over time.

### `plt.figure()`

Sets figure size.

### `plt.title()`

Adds title to graph.

### `plt.xlabel()` and `plt.ylabel()`

Labels graph axes.

### `plt.legend()`

Displays graph labels.

### `plt.show()`

Displays final graph.

### `plt.savefig()`

Saves graph as image.

**Use case:**
Saving forecast result graph.

---

## Interactive Visualization (Plotly)

### `go.Bar()`

Creates interactive bar charts.

**Use case:**
Top aircraft series visualization.

### `go.Scatter()`

Creates line and marker plots.

**Use case:**
Bombing dates vs temperature comparison.

### `go.Figure()`

Creates full plot object.

### `iplot()`

Displays interactive Plotly graphs.

### `scattergeo`

Used for world map plotting.

**Use case:**
Showing bombing takeoff bases and target locations on map.

---

## Date Handling

### `pd.to_datetime()`

Converts string date into datetime format.

**Use case:**
Used for time series analysis.

### `split()`

Splits date strings.

**Use case:**
Extracting year and month from mission dates.

---

## Time Series Analysis

### `adfuller()`

Performs Augmented Dickey-Fuller test.

**Use case:**
Checking whether the temperature data is stationary.

### `acf()`

Autocorrelation Function.

**Use case:**
Finding AR model order.

### `pacf()`

Partial Autocorrelation Function.

**Use case:**
Finding MA model order.

### Rolling Mean / Rolling Std

Used to check trend and stationarity.

**Use case:**
Stationarity checking before ARIMA.

---

## Forecasting

### `ARIMA()`

Builds ARIMA model for forecasting.

**Use case:**
Predicting future mean temperature values.

### `predict()`

Generates forecast values.

**Use case:**
Forecasting temperature trends.

---

## Model Evaluation

### `mean_squared_error()`

Calculates prediction error.

**Use case:**
Evaluating ARIMA model performance.

---

## Key Analysis Performed

* Country-wise bombing mission analysis
* Top target countries analysis
* Aircraft series comparison
* Takeoff base visualization on world map
* Bombing path mapping
* Theater of operations analysis
* Weather station location mapping
* Mean temperature trend analysis
* Bombing dates vs temperature comparison
* Stationarity testing
* ARIMA forecasting
* Forecast error evaluation

---

## Output

The project provides:

* Statistical insights
* Interactive maps
* Time series temperature graphs
* Bombing mission visualizations
* Weather forecasting graphs
* ARIMA prediction results

---

## Conclusion

This project combines **historical warfare data** with **weather analysis** to understand how environmental conditions may have affected World War II bombing missions.

It also demonstrates practical use of:

* Data Cleaning
* Exploratory Data Analysis
* Visualization
* Time Series Forecasting
* ARIMA Modeling

This makes the project a strong example of real-world Python data analysis and forecasting.

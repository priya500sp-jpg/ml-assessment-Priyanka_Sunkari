# Business Analysis – Retail Promotions

## 1. Problem Formulation

The objective of this problem is to predict the number of items sold in a retail store based on various factors such as promotions, store characteristics, and time-related features.

This is a **supervised learning regression problem**, where the target variable is `items_sold`.

Predicting items sold is more appropriate than revenue because revenue can vary due to pricing changes, whereas items sold directly reflects customer demand.

---

## 2. Data Understanding & Preparation

The dataset consists of multiple features such as store size, location type, promotion type, and transaction date.

### Data Preparation Steps:

* Missing values were handled using mean imputation.
* Categorical variables were encoded into numerical format using one-hot encoding.
* Date features were transformed into useful components such as:

  * Year
  * Month
  * Day of week
* The dataset was sorted by date to preserve time order.

### Data Granularity:

The data is maintained at a **store-day level**, meaning each row represents the number of items sold for a store on a particular day.

---

## 3. Exploratory Data Analysis (EDA)

EDA was performed to understand patterns in the data:

* Sales trends were analyzed across different promotion types.
* Store location and size were compared to identify their impact on sales.
* Time-based patterns such as weekday vs weekend sales were observed.

These insights help in identifying key drivers of sales.

---

## 4. Modeling Approach

A regression model was used to predict `items_sold`.

### Key Steps:

* Feature engineering was applied to improve input quality.
* Data was split using a **time-based split** instead of random split to avoid data leakage.
* Models such as Linear Regression and Random Forest were considered.

---

## 5. Evaluation Metrics

The model performance was evaluated using:

* **RMSE (Root Mean Squared Error)** – measures prediction error magnitude
* **MAE (Mean Absolute Error)** – measures average error

Random splitting was avoided because it can lead to unrealistic performance due to leakage in time-series data.

---

## 6. Deployment Strategy

The model can be deployed in a real-world system as follows:

* Save the trained model using serialization (e.g., pickle)
* Use it to predict future sales based on upcoming promotions
* Integrate into business dashboards for decision-making

---

## 7. Business Impact

This solution helps businesses:

* Optimize promotional strategies
* Forecast demand more accurately
* Improve inventory management
* Reduce stock shortages or overstock situations

---

## 8. Conclusion

By applying machine learning techniques and feature engineering, we were able to build a predictive system for retail sales.

The use of time-based validation ensures realistic performance, and the insights generated can support better business decisions.

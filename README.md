# Assessing Ideal U.S. Northeast States for Living

## Irith Chaturvedi  
**Email:** Irith2004@gmail.com  

---

## Introduction

### Motivation:
The Northeastern region of the USA comprises states including Pennsylvania, Maine, New York, New Jersey, Massachusetts, Connecticut, Rhode Island, New Hampshire, and Vermont. These states hold historical and cultural significance as a confluence of different populations. However, affordability remains a challenge for many residents. According to Daniel Parra (2023), "65% of Latino households have trouble with cost of living compared to 58% of Black households and 51% of Asians or Native Hawaiian/Pacific Islanders."

### Alternative Places in the U.S. Northeast:

#### Why Stay in the Northeast:
This project highlights the Northeast's historical prosperity, providing reassurance to those considering relocating, while also exploring more affordable alternatives.

#### Focus on Affordability:
The goal is to spotlight cities that won't strain the budget, providing viable options for career development without excessive costs.

#### Avoiding Newly Saturated Cities:
Instead of moving to popular Southern cities like Austin and Dallas, this project suggests considering sister cities for better career prospects.

#### Strategic Move from New York:
Encouraging individuals to make informed decisions when leaving New York by exploring nearby cities with growth potential to ensure a smooth transition.

---

## Methods

### Data Retrieval:
Four datasets were used for analysis:
- **Per Capita Income per US State** (Kaggle)
- **Updated House Prices of Northeastern US States** (Kaggle)
- **Population Statistics of US States, Territories, and Regions** (Data.gov)
- **Pittsburgh Home Prices Dataset** (census.data.gov)

### Data Cleaning:
- Null and empty records were removed.
- Unwanted columns were dropped.
- For machine learning, only "price" and "neighborhood" columns were used from the Pittsburgh dataset.

### Data Sorting:
- Datasets were grouped based on US states.
- Population change dataset was filtered to include only 2010 and 2019 to establish a significant trend over a decade.

### Analysis and Visualizations:
- **Python PANDAS** was used for data manipulation.
- **Folium** was used to create spatial visualizations with state borders as map outlines.
- **Matplotlib** was used for double bar plots to compare population trends over time.
- **Correlation Coefficient Table** was created to analyze variable relationships.

### Machine Learning Model:
- A **Logistic Regression** model was used to predict the best Pittsburgh neighborhood based on a given budget.
- **Training Data:** Included best neighborhoods and current listings.
- **Pipeline Creation:**
  - `StandardScaler()`: Standardized features.
  - `LogisticRegression()`: Trained the logistic regression model.
- **Hyperparameter Tuning:**
  - `GridSearchCV` was used for optimization with 5-fold cross-validation.

### Data Reshaping:
- `X_train_reshaped` and `y_train_reshaped` were converted into NumPy arrays for compatibility with the pipeline.

### Model Fitting and Evaluation:
- The model was trained using `GridSearchCV` to determine the best hyperparameters.
- When a budget value is supplied, the model returns the best Pittsburgh neighborhood that fits the financial criteria.

---

## Results

### Population Trends and Cost of Living:
- The Southern U.S. has experienced significant population growth due to a more reasonable cost of living compared to New York.
- Migration trends show that areas with reasonable living costs attract higher populations.
- Cities with a strong job market and moderate living costs are more favorable for international migration.
- Northeastern states, excluding New York, are preferred due to stable average income levels relative to living costs.

### Recommended Cities:
#### 1. **Pittsburgh, Pennsylvania**
- **Average House Price:** $160K
- **Diverse Population:** 22% Black/African American, 5.5% Asian
- **Average Salary for White-Collar Jobs:** $64K
- **Why Pittsburgh?** Offers economic stability and an affordable alternative to NYC without a drastic lifestyle change.

#### 2. **Hartford, Connecticut**
- **Average House Price:** $190K
- **Diverse Population:** 34% Black/African American, 20% Hispanic
- **Competitive Salaries for White-Collar Jobs**
- **Why Hartford?** A balance of affordability, diversity, and job opportunities make it a viable relocation option from NYC.

---

## Conclusion
This study identifies ideal cities in the U.S. Northeast for relocation based on employment opportunities, housing affordability, and economic stability. The goal is to assist individuals leaving NYC in finding suitable alternatives that maintain economic efficiency while reducing cost burdens. Pittsburgh and Hartford emerge as the top recommendations due to their reasonable housing prices, strong job markets, and cultural diversity.

---

## References
- City Limits. (2023, April 26). *More Than Half of Immigrant New Yorkers Can't Afford Basic Needs, Report Finds.* Retrieved from [City Limits](https://citylimits.org/2023/04/26/more-than-half-of-immigrant-new-yorkers-cant-afford-basic-needs-report-finds/)
- Kaggle. (n.d.). *USA Real Estate Dataset.* Retrieved from [Kaggle](https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset)
- Kaggle. (n.d.). *United States Counties by Per Capita Income.* Retrieved from [Kaggle](https://www.kaggle.com/datasets/kabhishm/united-states-counties-by-per-capita-income)
- U.S. Census Bureau. (n.d.). *Population Estimates Program: 2010s State Total.* Retrieved from [Census.gov](https://www.census.gov/data/datasets/time-series/demo/popest/2010s-state-total.html)
- Data USA. (n.d.). *Pittsburgh, PA.* Retrieved from [Data USA](https://datausa.io/profile/geo/pittsburgh-pa/)
- Data USA. (n.d.). *Hartford, CT.* Retrieved from [Data USA](https://datausa.io/profile/geo/hartford-ct/)
- Redfin. (n.d.). *Shadyside Housing Market, Pittsburgh, PA.* Retrieved from [Redfin](https://www.redfin.com/neighborhood/156434/PA/Pittsburgh/Shadyside/housing-market)
- Data.gov. (n.d.). *Property Data with Geographic Identifiers.* Retrieved from [Data.gov](https://catalog.data.gov/dataset/property-data-with-geographic-identifiers)

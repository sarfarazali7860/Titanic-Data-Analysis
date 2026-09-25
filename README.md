# Titanic Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project presents a complete **Exploratory Data Analysis (EDA)** of the Titanic passenger dataset using Python.

The purpose of this project is to understand the dataset, identify data-quality issues, clean the data, explore individual variables, analyze relationships between variables, visualize important patterns, and identify factors associated with passenger survival.

The complete analysis was performed using **Google Colab** and Python.

## 🎯 Project Objectives
The main objectives of this project are to:
* Understand the structure of the Titanic dataset
* Explore the dataset using descriptive statistics
* Identify missing values and data-quality issues
* Check for duplicate records
* Clean and prepare the dataset
* Create new useful features
* Perform univariate analysis
* Perform bivariate analysis
* Perform multivariate analysis
* Analyze correlations between numerical variables
* Compare survival across different passenger groups
* Answer important analytical questions
* Extract meaningful insights from the data

## 📊 Dataset
The Titanic dataset contains information about passengers who were aboard the Titanic.

### Dataset Features

| Column        | Description                                        |
| ------------- | -------------------------------------------------- |
| `PassengerId` | Unique identification number of each passenger     |
| `Survived`    | Survival status (0 = No, 1 = Yes)                  |
| `Pclass`      | Passenger class (1 = First, 2 = Second, 3 = Third) |
| `Name`        | Passenger name                                     |
| `Sex`         | Passenger gender                                   |
| `Age`         | Passenger age                                      |
| `SibSp`       | Number of siblings/spouses aboard                  |
| `Parch`       | Number of parents/children aboard                  |
| `Ticket`      | Ticket number                                      |
| `Fare`        | Passenger fare                                     |
| `Cabin`       | Cabin information                                  |
| `Embarked`    | Port from which the passenger embarked             |


# 🔧 Tools and Technologies

The following tools and Python libraries were used:

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Google Colab**
* **Jupyter Notebook**
* **GitHub**


# 📁 Project Structure

```text
titanic-eda/
│
├── README.md
├── titanic_eda.ipynb
│
└── data/
    └── titanic.csv
```

### Files

**`README.md`**
Contains the documentation and overview of the project.

**`titanic_eda.ipynb`**
Contains the complete Python code, visualizations, analysis, and interpretations.

**`data/titanic.csv`**
Contains the Titanic dataset used for the analysis.

---

# 1️⃣ Importing Libraries

The following libraries were imported for data analysis and visualization:

* Pandas for data manipulation
* NumPy for numerical operations
* Matplotlib for visualization
* Seaborn for statistical visualization

---

# 2️⃣ Loading the Dataset

The Titanic dataset was loaded into a Pandas DataFrame using `read_csv()`.

The DataFrame was then used throughout the project for data exploration and analysis.

---

# 3️⃣ Dataset Overview

The dataset was explored using different methods to understand its structure.

The following operations were performed:

* Displayed the first few rows
* Displayed the last few rows
* Checked dataset shape
* Examined column names
* Checked data types
* Generated statistical summaries

### Purpose

This step provided an initial understanding of the dataset before performing cleaning and analysis.

---

# 4️⃣ Data Quality Assessment

The dataset was checked for common data-quality problems.

The following checks were performed:

* Missing values
* Duplicate records
* Data types
* Numerical summaries
* Categorical distributions

### Missing Values

Missing values were identified in columns such as:

* `Age`
* `Cabin`
* `Embarked`

The amount of missing data was examined before deciding how to handle each column.

---

# 5️⃣ Data Cleaning

Data cleaning was performed to prepare the dataset for analysis.

### Missing Age Values

Missing values in the `Age` column were filled using the **median age**.

### Missing Embarked Values

Missing values in `Embarked` were filled using the **mode**.

### Cabin Column

The `Cabin` column contained a large number of missing values, so it was removed from the cleaned analysis dataset.

### Cleaned Dataset

A copy of the original dataset was created before performing the cleaning operations so that the original data remained unchanged.

---

# 6️⃣ Feature Engineering

New features were created to make the analysis more meaningful.

### Family Size

A new `FamilySize` feature was created using:

```text
FamilySize = SibSp + Parch + 1
```

This represents the total number of family members traveling with each passenger, including the passenger themselves.

### Is Alone

An `IsAlone` feature was created:

* `1` = Passenger was traveling alone
* `0` = Passenger was traveling with family

### Age Group

Passengers were grouped into different age categories:

* Child
* Teenager
* Young Adult
* Adult
* Senior

### Fare Group

Passengers were also divided into fare groups using quartiles:

* Low
* Medium
* High
* Very High

---

# 7️⃣ Univariate Analysis

Univariate analysis examines one variable at a time.

The following variables were explored:

* Survival
* Gender
* Passenger class
* Age
* Fare
* Family size
* Age groups

### Visualizations

Different plots were used, including:

* Count plots
* Histograms
* Distribution plots

### Purpose

The purpose of univariate analysis was to understand the distribution and characteristics of individual variables.

---

# 8️⃣ Survival Analysis

The distribution of the `Survived` variable was analyzed.

The variable contains:

* `0` = Did not survive
* `1` = Survived

The analysis showed the overall distribution of passengers who survived and those who did not.

---

# 9️⃣ Gender Analysis

The number of male and female passengers was examined.

The survival rate was also compared between genders.

### Finding

Female passengers had a considerably higher survival rate than male passengers in the dataset.

---

# 🔟 Passenger Class Analysis

The distribution of passengers across the three passenger classes was analyzed.

The classes were:

* First Class
* Second Class
* Third Class

Survival rates were then compared across the three classes.

### Finding

Passengers in higher classes had higher survival rates than passengers in lower classes.

---

# 1️⃣1️⃣ Age Analysis

The distribution of passenger ages was examined using histograms and statistical summaries.

The analysis helped identify:

* Typical passenger age
* Age distribution
* Young passengers
* Older passengers
* Differences in age across survival groups

---

# 1️⃣2️⃣ Fare Analysis

Passenger fares were analyzed using statistical summaries and distribution plots.

The relationship between passenger class and fare was also examined.

### Finding

First-class passengers generally paid higher fares than passengers in second and third class.

---

# 1️⃣3️⃣ Bivariate Analysis

Bivariate analysis examines the relationship between two variables.

The following relationships were analyzed:

* Sex vs Survival
* Pclass vs Survival
* Age vs Survival
* Age Group vs Survival
* Family Size vs Survival
* Is Alone vs Survival
* Pclass vs Fare

### Purpose

The purpose was to understand how different passenger characteristics were associated with survival.

---

# 1️⃣4️⃣ Multivariate Analysis

Multivariate analysis examines relationships involving multiple variables.

Examples included:

* Passenger class + gender + survival
* Age + gender + survival
* Passenger class + survival

These analyses helped provide a deeper understanding of survival patterns.

---

# 1️⃣5️⃣ Correlation Analysis

A correlation matrix was created to examine relationships between numerical variables.

The correlation coefficient ranges from:

```text
-1 to +1
```

### Interpretation

* `+1` → Perfect positive relationship
* `0` → No linear relationship
* `-1` → Perfect negative relationship

The correlation heatmap was used to visually identify the strength and direction of relationships between numerical variables.

### Important Observation

`Pclass` showed a negative correlation with `Survived`.

This indicates that as the numerical class value increased from 1 toward 3, survival tended to decrease.

Correlation shows association between variables and does not by itself prove causation.

---

# 1️⃣6️⃣ Statistical Analysis

Descriptive statistics were used to understand numerical variables.

The analysis included:

* Mean
* Median
* Standard deviation
* Minimum
* Maximum
* Quartiles

These statistics helped summarize variables such as:

* Age
* Fare
* Family size

---

# 1️⃣7️⃣ Analytical Questions

The analysis addressed several important questions:

### 1. What percentage of passengers survived?

The overall survival distribution was analyzed to determine the proportion of passengers who survived.

### 2. Did gender relate to survival?

Survival rates were compared between male and female passengers.

### 3. How did passenger class relate to survival?

Survival rates were compared across first, second, and third class.

### 4. How was age distributed among passengers?

The age distribution was examined using descriptive statistics and visualizations.

### 5. Did age differ between survivors and non-survivors?

Age distributions were compared across survival groups.

### 6. How did fare differ across passenger classes?

Average fares were compared between passenger classes.

### 7. Did family size relate to survival?

Survival rates were examined across different family sizes.

### 8. Did traveling alone relate to survival?

Passengers traveling alone were compared with passengers traveling with family.

### 9. Which numerical variables were correlated?

A correlation matrix was created to identify relationships between numerical variables.

---

# 📌 Key Findings

The main observations from the analysis were:

1. **Gender was strongly associated with survival.**
   Female passengers had a much higher survival rate than male passengers.

2. **Passenger class was associated with survival.**
   First-class passengers had higher survival rates than passengers in lower classes.

3. **Passenger class and survival had a negative correlation.**
   Because `Pclass` is numerically represented as 1, 2, and 3, higher numerical values correspond to lower passenger classes.

4. **Fare differed substantially between passenger classes.**
   First-class passengers generally paid higher fares.

5. **Age showed differences across survival groups.**
   The age distribution was not identical between survivors and non-survivors.

6. **Family-related variables provided additional information about survival patterns.**
   Family size and traveling-alone status were explored to understand their association with survival.

---

# 📈 Visualizations

The project includes several visualizations, including:

* Survival count plot
* Gender distribution
* Passenger class distribution
* Age distribution
* Fare distribution
* Survival by gender
* Survival by passenger class
* Survival by age
* Survival by age group
* Survival by family size
* Survival by traveling alone
* Multivariate plots
* Correlation heatmap

These visualizations were used to make patterns in the data easier to understand.

---

# 🧠 Skills Demonstrated

This project demonstrates practical skills in:

* Python programming
* Pandas
* NumPy
* Data cleaning
* Missing-value handling
* Feature engineering
* Exploratory Data Analysis
* Descriptive statistics
* Data visualization
* Correlation analysis
* Analytical thinking
* Data interpretation
* Working with Google Colab
* GitHub project organization

---

# 🏁 Conclusion

The Titanic EDA project provided practical experience with the complete exploratory data-analysis workflow.

The project started with understanding the dataset and checking its quality. Missing values and unnecessary data were then handled before creating additional features such as `FamilySize`, `IsAlone`, `AgeGroup`, and `FareGroup`.

Univariate, bivariate, and multivariate analyses were performed to explore patterns in the data. Correlation analysis was also used to examine relationships between numerical variables.

Overall, the analysis demonstrated how Python and data-visualization libraries can be used to explore a real-world dataset and extract meaningful insights from it.

---

# 👨‍💻 Author

**Sarfaraz Ali**

BS Information Technology Student

### Technologies Used

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Google Colab` · `GitHub`

---

## 📚 Project Purpose

This project was created as part of my learning journey in **Data Analysis and Data Science** and is intended for educational and portfolio purposes.


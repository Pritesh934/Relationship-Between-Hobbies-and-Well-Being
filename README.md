# 🧘 The Relationship Between Hobbies and Well-Being

This project investigates the impact of students' hobbies, daily habits, and lifestyle choices on their overall well-being, social connections, and academic performance (GPA). By analyzing survey data, we aim to uncover whether active engagement in hobbies correlates with better academic outcomes or distinct personality traits.

## 📂 Project Overview

University life involves balancing academics, social activities, and personal interests. This data science project explores these dynamics through statistical modeling and machine learning.

**Key Research Questions:**
1.  **GPA & Hobbies**: Do students with active hobbies (arts, music, sports) have higher GPAs?
2.  **Predicting Performance**: Can we predict GPA based on hobby type, study habits, and personality?
3.  **Lifestyle Clustering**: Are there distinct clusters of students based on their sleep, study, and leisure patterns?
4.  **Personality Traits**: Are extroverts more likely to engage in multiple hobbies compared to introverts?

## 📊 Dataset

The project uses a custom dataset collected via survey, containing **68 variables** from student respondents.

**Key Features:**
* **Demographics**: Age, Gender, Height, Weight.
* **Academic**: GPA, Hours spent studying, Courses taken.
* **Lifestyle**: Hobbies, Hours on Social Media, Sleep duration, Exercise habits.
* **Preferences**: Beverage preference, Cuisine, Indoor/Outdoor preference.
* **Personality**: Introvert/Extrovert status, Social butterfly (Party Person).

*Filename: `Project_dataset.xlsx - Form Responses 1.csv`*

## 🛠️ Technologies & Libraries Used

The analysis is implemented in Python using a Jupyter Notebook. Key tools include:

* **Pandas & NumPy**: For data cleaning (handling missing values, unit conversion for Height/Weight) and manipulation.
* **Matplotlib & Seaborn**: For Exploratory Data Analysis (EDA), correlation heatmaps, and distribution plots.
* **Scikit-learn**:
    * `LinearRegression` & `LogisticRegression`: For predictive modeling.
    * `KMeans`: For clustering analysis.
    * `StandardScaler` & `OneHotEncoder`: For preprocessing features.
* **Statsmodels**: For detailed statistical summaries (OLS regression).

## 🧠 Methodology & Models

The project employs four main analytical approaches:

1.  **Linear Regression**:
    * *Goal*: Analyze the direct relationship between "Active Hobbies" and GPA.
    * *Result*: Found a positive but statistically insignificant correlation, suggesting hobbies alone don't guarantee higher grades.

2.  **Multiple Linear Regression**:
    * *Goal*: Predict GPA using a combination of Study Hours, Hobbies, and Personality Type.
    * *Result*: The model showed that these variables combined explain only a small fraction of the variance in GPA.

3.  **K-Means Clustering**:
    * *Goal*: Group students based on lifestyle habits (Sleep vs. Study Hours).
    * *Result*: Identified distinct student profiles (e.g., "Balanced", "High Study/Low Sleep"), revealing that excessive studying without sleep does not necessarily lead to the highest GPAs.

4.  **Logistic Regression (Classification)**:
    * *Goal*: Classify students as "Introvert" or "Extrovert" based on their number of hobbies.
    * *Result*: The number of hobbies was not a strong predictor of personality type; Ambiverts often reported the highest number of hobbies.

## 🚀 How to Run

1.  **Clone this repository**.
2.  **Install dependencies**:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
    ```
3.  **Open the Jupyter Notebook**:
    ```bash
    jupyter notebook "05_Project_Code.ipynb"
    ```
4.  **Load the Data**:
    * Ensure `Project_dataset.xlsx - Form Responses 1.csv` is in the same directory.
    * Run the cells sequentially to perform data cleaning, visualization, and modeling.

## 📈 Key Results & Findings

The analysis produced several interesting insights regarding student life, academic performance, and personality traits:

### 1. Hobbies vs. Academic Performance (Linear Regression)
* **Hypothesis**: Students with active hobbies (e.g., sports, music, arts) have higher GPAs.
* **Result**: The analysis showed a **positive but statistically insignificant** relationship between active hobbies and GPA.
* **Insight**: While students engaged in hobbies tended to have slightly higher GPAs, the correlation was weak, suggesting that having a hobby is not a guaranteed predictor of academic success.

### 2. Predicting GPA (Multiple Linear Regression)
* **Hypothesis**: A combination of study habits, hobby type, and personality can accurately predict a student's GPA.
* **Result**: The model explained only a small fraction of the variance in GPA. None of the selected variables (Study Hours, Hobbies, Personality Type) were strong individual predictors.
* **Insight**: Academic performance is likely influenced by other unmeasured factors (e.g., time management, prior knowledge, motivation) rather than just the number of hours studied or hobbies pursued.

### 3. Student Lifestyle Profiles (K-Means Clustering)
* **Hypothesis**: Students fall into distinct lifestyle clusters based on sleep and study habits.
* **Result**: The clustering algorithm identified specific student profiles:
    * **Balanced Achievers**: Students with balanced sleep and study schedules tended to have high GPAs (**~3.65**).
    * **Overworked Students**: A cluster of students studying excessive hours (**~81.7 hours/week**) did *not* show proportionally higher GPAs, indicating diminishing returns on over-studying.

### 4. Personality & Hobbies (Logistic Regression)
* **Hypothesis**: Extroverts engage in more hobbies than introverts.
* **Result**: The classification model found **no significant relationship** between the sheer number of hobbies and being an extrovert.
* **Insight**: Surprisingly, **Ambiverts** (students identifying as both introverted and extroverted) reported the highest average number of hobbies, contrary to the belief that extroverts are the most active.

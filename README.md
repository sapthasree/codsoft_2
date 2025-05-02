# codsoft_2
# Movie Rating Prediction

This project focuses on building a machine learning model to predict movie ratings based on various attributes such as year, duration, genre, director, and main actors. The project was completed as part of my Data Science Internship at **Codsoft**.

## Objective

To predict IMDb-style movie ratings using linear regression and evaluate the model's performance with the Mean Absolute Error (MAE).

## Dataset

- Source: `movie.csv`
- Records: 15,509 movies
- Attributes: Name, Year, Duration, Genre, Rating, Votes, Director, Actor 1, Actor 2, Actor 3

## Key Steps

### 1. Data Preprocessing

- Loaded data with `pandas`, handled encoding issues.
- Checked and removed rows with missing values in crucial columns:
  - `Year`, `Duration`, `Genre`, `Rating`, `Votes`, `Director`, `Actor 1`, `Actor 2`, `Actor 3`

### 2. Data Cleaning

- Removed 'min' from `Duration` and converted to float.
- Extracted 4-digit year values using regex.
- Removed leading negative signs from years.
- Converted `Votes` to float after removing commas.

### 3. Label Encoding

- Categorical columns encoded using `LabelEncoder`:
  - `Genre`, `Director`, `Actor 1`, `Actor 2`, `Actor 3`

### 4. Model Building

- Defined features (`X`) and target (`y`) where:
  - `X = all columns except 'Name' and 'Rating'`
  - `y = Rating`
- Split data into train-test sets (80/20 split).
- Applied Linear Regression using `sklearn.linear_model`.

### 5. Model Evaluation

- Predicted on test set.
- Evaluated using **Mean Absolute Error**.
- Output:
  - **MAE** = `1.0495` (approx)

### 6. Result Matrix

Printed a matrix comparing true ratings with predicted values.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook

## Outcome

Successfully developed a linear regression model that predicts movie ratings with a Mean Absolute Error of approximately **1.05**, demonstrating a solid grasp of regression modeling and data preprocessing.

## Internship Info

- **Organization**: Codsoft  
- **Role**: Data Science Intern  
- **Duration**: 15/04/25 to 15/05/25.  
- **Tools Used**: Jupyter, Python, Scikit-learn

---

# Video Game Sales Analysis & Prediction

This project focuses on analyzing historical video game sales data and building a robust machine learning pipeline to predict global sales based on game metadata.[cite: 1]

## 📌 Project Overview
The objective of this project is to process the `vgsales.csv` dataset and develop a model that can estimate a game's commercial success using only pre-release information such as platform, genre, and publisher.[cite: 1] A key component of this study is the identification and prevention of **Data Leakage** in predictive modeling.[cite: 1]

## ⚙️ Technical Workflow
The analysis is performed within the `VGA.ipynb` notebook and follows a structured data science approach:[cite: 1]

### 1. Data Cleaning & Preprocessing
*   **Handling Missing Values**: Missing year values are filled using the median year for their respective platforms to maintain data consistency.[cite: 1]
*   **Publisher Imputation**: Rows with missing publisher information are filled with the label 'Unknown'.[cite: 1]
*   **Feature Engineering**: Categorical variables (Platform, Genre, Publisher) are converted into numerical format using one-hot encoding for model compatibility.[cite: 1]

### 2. Exploratory Data Analysis (EDA)
*   **Sales Distributions**: Histograms are used to visualize the spread of regional and global sales.[cite: 1]
*   **Market Trends**: Bar charts identify the most successful genres and platforms in terms of total global sales.[cite: 1]
*   **Correlation Matrix**: A heatmap visualization is used to inspect the correlation between North American, European, and Japanese sales figures.[cite: 1]

### 3. The Data Leakage Demonstration
*   The project highlights a common pitfall in sales prediction: using regional sales (NA, EU, JP) to predict Global Sales.[cite: 1]
*   **Leaky Pipeline**: A demonstration shows how including regional sales leads to an unrealistically high $R^2$ score because the target is essentially a sum of those features.[cite: 1]
*   **Clean Pipeline**: A realistic modeling setup is established using only metadata—Platform, Year, Genre, and Publisher—ensuring the model can be used *before* a game goes to market.[cite: 1]

## 🛠️ Requirements
The project is built using the following Python libraries:[cite: 1]
*   `pandas`
*   `matplotlib`
*   `numpy`
*   `scikit-learn`

## 📂 Dataset
The repository includes:
*   `vgsales.csv`: The raw dataset containing sales data for over 16,000 games.[cite: 1]
*   `VGA.ipynb`: The primary notebook containing all analysis, cleaning, and model development code.[cite: 1]

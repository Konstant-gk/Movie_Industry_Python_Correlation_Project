## 📊 Project Overview

This project performs a comprehensive correlation analysis on movie industry data to identify key factors that influence box office success. Using Python's data science libraries, I analyzed over 7,600 movies to uncover relationships between budget, gross earnings, ratings, votes, and other critical metrics.

## 🎯 Objective

The primary objective of this analysis is to answer the question: **What factors are most strongly correlated with a movie's financial success (gross earnings)?**

By examining correlations between various movie attributes, this project provides actionable insights for:
- **Film Studios**: Understanding which investments (budget, casting, genre) yield the highest returns
- **Investors**: Identifying patterns that predict box office performance
- **Filmmakers**: Making data-driven decisions about production elements

## 📈 Key Metrics Analyzed

### Financial Metrics
- **Budget**: Production costs in USD
- **Gross Earnings**: Total box office revenue in USD

### Performance Metrics
- **IMDb Score**: Average user rating (0-10 scale)
- **Votes**: Number of user ratings received
- **Runtime**: Movie duration in minutes

### Categorical Features
- **Genre**: Movie category (Action, Drama, Comedy, etc.)
- **Rating**: MPAA rating (PG, PG-13, R, etc.)
- **Company**: Production studio
- **Country**: Production country
- **Year**: Release year

## 🔍 Methodology

### 1. Data Loading & Exploration
- Loaded dataset containing 7,668 movie records
- Performed initial data exploration to understand structure
- Identified missing values and data quality issues

### 2. Data Cleaning & Preprocessing
- **Missing Value Analysis**: Calculated percentage of missing data per column
  - Budget: 28.3% missing
  - Gross: 2.5% missing
  - Other columns: <1% missing
- **Data Type Conversion**: 
  - Converted budget, gross, votes, and runtime to appropriate numeric types
  - Handled NaN values appropriately for correlation analysis
- **Feature Engineering**:
  - Extracted release year from date strings using regex pattern matching
  - Created `yearcorrect` column for accurate temporal analysis

### 3. Correlation Analysis

#### Numeric Features Correlation
- Calculated Pearson correlation coefficients for all numeric variables
- Created correlation matrix heatmap for visual analysis
- Identified strong positive correlations:
  - **Budget ↔ Gross Earnings**: Strong positive correlation
  - **Votes ↔ Gross Earnings**: Strong positive correlation
  - **Budget ↔ Votes**: Moderate positive correlation

#### Categorical Features Correlation
- Converted categorical variables (genre, company, country, etc.) to numeric codes
- Analyzed correlations between categorical and numeric features
- Discovered relationships between genre, company, and financial performance

### 4. Visualization

#### Scatter Plots
- **Budget vs. Gross Earnings**: Visualized relationship with scatter plot
- **Regression Analysis**: Added regression line to show trend

#### Correlation Heatmaps
- Created annotated heatmaps showing correlation strength
- Color-coded for easy interpretation (red = negative, blue = positive)

#### Correlation Pairs Analysis
- Unstacked correlation matrix to create sorted pairs
- Identified top correlations for detailed examination

## 📊 Key Findings

### Strong Correlations
1. **Budget and Gross Earnings**: Highest positive correlation
   - Higher budgets generally lead to higher gross earnings
   - Investment in production quality pays off

2. **Votes and Gross Earnings**: Strong positive correlation
   - Popular movies (more votes) tend to earn more
   - Audience engagement drives revenue

3. **Budget and Votes**: Moderate positive correlation
   - Big-budget films attract more audience attention
   - Marketing and production quality increase visibility

### Weak/No Correlations
- **Company and Gross Earnings**: Minimal correlation
  - Studio brand alone doesn't guarantee success
  - Content quality matters more than studio reputation

### Insights
- **Investment Strategy**: Budget allocation is a strong predictor of financial success
- **Audience Engagement**: Movies that generate more votes (discussion/buzz) perform better financially
- **Genre Impact**: Certain genres show different correlation patterns with financial metrics

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Basic plotting and visualization
- **Seaborn**: Statistical data visualization
- **Jupyter Notebook**: Interactive development environment

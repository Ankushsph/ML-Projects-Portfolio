# Pandas Data Analysis Projects

A collection of comprehensive data analysis projects using Pandas, demonstrating advanced data manipulation, feature extraction, and statistical analysis techniques.

## 📊 Overview

This repository contains two major data analysis projects that showcase real-world applications of Pandas for data manipulation, feature engineering, and statistical analysis. Each project demonstrates different aspects of data science workflow.

## 📁 Projects

### 1. [Countries Data Analysis](DataCapstone.ipynb)

**Global Country Dataset Analysis**
- **Dataset**: Countries.csv with 194 countries and 64 features
- **Scope**: Comprehensive analysis of global country data
- **Techniques**: Data exploration, statistical analysis, filtering, grouping

#### Key Features Analyzed:
- **Demographics**: Population, capital cities, regions, continents
- **Economic**: GDP, inflation, unemployment, tax revenue
- **Geographic**: Latitude, longitude, land area, agricultural land
- **Political**: Democracy scores, political leaders, government structure
- **Infrastructure**: Electricity access, energy production, transportation

#### Sample Analysis Questions:
```python
# Population analysis
df[df['population'] == df['population'].max()]  # Highest population
df[df['population'] == df['population'].min()]  # Lowest population

# Democratic analysis
df.sort_values(by='democracy_score', ascending=False)  # Top democratic countries

# Regional analysis
df['region'].value_counts()  # Countries per region
df[df['region'] == "Eastern Europe"]  # Eastern European countries
```

### 2. [Anime Dataset Feature Extraction](FeatureExtraction.ipynb)

**Anime Data Feature Engineering**
- **Dataset**: Anime.csv with comprehensive anime information
- **Focus**: Advanced feature extraction and data preprocessing
- **Techniques**: String manipulation, date parsing, feature creation

#### Feature Extraction Examples:

##### Episode Count Extraction
```python
def extract_episodes(txt):
    check = False
    data = ""
    for i in txt:
        if check and i == ")":
            check = False
            return data
        if check == True:
            data = data + i
        if i == "(":
            check = True
```

##### Time Period Analysis
```python
def calculate_total_months(period):
    try:
        start_str, end_str = period.split(' - ')
        start_date = datetime.strptime(start_str, '%b %Y')
        end_date = datetime.strptime(end_str, '%b %Y')
        r = relativedelta(end_date, start_date)
        return r.years * 12 + r.months + 1
    except:
        return None
```

#### Analysis Results:
- **Highest Scoring Anime**: Identified top-rated anime
- **Episode Count Analysis**: Found anime with most episodes
- **Duration Analysis**: Calculated running periods in months
- **Statistical Insights**: Score distributions and patterns

## 🛠️ Technical Skills Demonstrated

### Data Manipulation
- **Data Loading**: CSV file handling with Pandas
- **Data Exploration**: Shape, info, describe methods
- **Data Cleaning**: Handling missing values, duplicates
- **Data Filtering**: Conditional filtering and boolean indexing

### Feature Engineering
- **String Processing**: Text extraction and manipulation
- **Date Parsing**: Converting text dates to datetime objects
- **Categorical Encoding**: Creating dummy variables
- **Mathematical Operations**: Statistical calculations

### Statistical Analysis
- **Descriptive Statistics**: Mean, median, mode, standard deviation
- **Data Distribution**: Value counts, unique values
- **Correlation Analysis**: Finding relationships between variables
- **Grouping Operations**: Groupby operations and aggregations

## 📈 Key Insights

### Countries Analysis
- **Population Distribution**: Wide range from smallest to largest countries
- **Regional Patterns**: Different economic and political patterns by region
- **Democratic Scores**: Variation in democratic governance worldwide
- **Economic Indicators**: GDP, inflation, and employment correlations

### Anime Analysis
- **Rating Patterns**: Distribution of anime scores
- **Episode Trends**: Relationship between episode count and ratings
- **Duration Analysis**: Long-running vs. short series patterns
- **Feature Relationships**: Correlations between different anime attributes

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn python-dateutil
```

### Running the Projects
1. **Countries Analysis**:
   ```bash
   jupyter notebook DataCapstone.ipynb
   ```

2. **Anime Feature Extraction**:
   ```bash
   jupyter notebook FeatureExtraction.ipynb
   ```

## 📊 Data Sources

### Countries Dataset
- **Size**: 194 countries × 64 features
- **Features**: Demographics, economics, geography, politics
- **Use Cases**: Global analysis, country comparisons, regional studies

### Anime Dataset
- **Content**: Anime titles, scores, episodes, time periods
- **Features**: Title parsing, episode extraction, duration calculation
- **Use Cases**: Entertainment analysis, feature engineering examples

## 🎯 Learning Outcomes

After completing these projects, you will be able to:

- ✅ **Data Exploration**: Comprehensive EDA techniques
- ✅ **Feature Engineering**: Advanced text and date processing
- ✅ **Statistical Analysis**: Descriptive and inferential statistics
- ✅ **Data Cleaning**: Handling real-world data issues
- ✅ **Visualization**: Creating meaningful data visualizations
- ✅ **Problem Solving**: Tackling complex data analysis challenges

## 🔧 Advanced Techniques Used

### String Manipulation
```python
# Complex text extraction
def extraction_time(txt):
    check = False
    data = ""
    for i in range(len(txt)):
        if txt[i] == ')':
            for j in range(i+1, i+20):
                data += txt[j]
            break
    return data
```

### Date Processing
```python
# Date range calculations
from dateutil.relativedelta import relativedelta
from datetime import datetime

def calculate_total_months(period):
    start_str, end_str = period.split(' - ')
    start_date = datetime.strptime(start_str, '%b %Y')
    end_date = datetime.strptime(end_str, '%b %Y')
    r = relativedelta(end_date, start_date)
    return r.years * 12 + r.months + 1
```

### Data Aggregation
```python
# Complex grouping operations
df.groupby('region')['population'].agg(['mean', 'median', 'std'])
df['region'].value_counts()
```

## 📝 Project Structure

```
panadas/
├── README.md                 # This file
├── DataCapstone.ipynb       # Countries analysis
├── FeatureExtraction.ipynb  # Anime feature engineering
├── Countries.csv            # Countries dataset
└── anime.csv               # Anime dataset
```

## 🎓 Educational Value

These projects demonstrate:
- **Real-world Data**: Working with actual datasets
- **Problem-solving**: Breaking down complex analysis tasks
- **Code Quality**: Clean, documented, and reusable code
- **Statistical Thinking**: Applying statistical concepts to data
- **Feature Engineering**: Creating meaningful features from raw data

## 🔗 Related Projects

- [NumPy Learning](../numpy/)
- [Machine Learning Projects](../)
- [Heart Disease Prediction](../heart_app/)

## 📄 License

This educational content is part of the ML Projects Portfolio. See main README for license information.

---

**Author**: Ankushsph  
**GitHub**: [https://github.com/Ankushsph](https://github.com/Ankushsph)  
**Purpose**: Advanced Pandas data analysis examples and tutorials

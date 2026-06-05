# Netflix Content Analysis Dashboard (2010–2025)

## Project Overview

The Netflix Content Analysis Dashboard is an interactive Business Intelligence project developed using Power BI to analyze Netflix's content library from 2010 to 2025. The dashboard provides valuable insights into content distribution, genre popularity, language diversity, country-wise production, IMDb rating trends, and yearly content growth.

This project demonstrates data cleaning, transformation, data modeling, DAX calculations, and dashboard design skills to convert raw Netflix data into meaningful business insights.

---

## Problem Statement

Netflix offers thousands of movies and TV shows across different countries, languages, and genres. Understanding content distribution and performance trends is essential for identifying audience preferences and supporting strategic business decisions.

This dashboard aims to answer the following questions:

- How many Movies and TV Shows are available on Netflix?
- Which genres dominate Netflix's catalog?
- Which countries contribute the most content?
- What are the most common languages available?
- How are IMDb ratings distributed?
- How has Netflix's content library grown over time?
- Which titles have the highest popularity?

---

## Dashboard Preview

<img width="100%" alt="Netflix Dashboard" src="Images/dashboard-overview.png">

---

## Key Performance Indicators (KPIs)

| Metric | Value |
|----------|----------|
| Total Contents | 28,396 |
| Total Movies | 13,895 |
| Total TV Shows | 14,988 |
| Total Countries | 146 |
| Total Languages | 81 |

---

## Dashboard Features

### Interactive Filters

Users can filter dashboard insights by:

- Content Type
- Genre
- Language

### Visualizations

#### Movies vs TV Shows
Compares the percentage distribution of movies and television shows available on Netflix.

#### IMDb Rating Distribution
Analyzes content based on rating ranges to understand quality trends.

#### Top Countries by Number of Titles
Shows countries contributing the highest number of Netflix titles.

#### Top Languages
Displays the most common languages available across Netflix content.

#### Top Genres
Identifies the most popular genres in the Netflix catalog.

#### Top 5 Popular Titles
Highlights the most popular Netflix titles based on popularity metrics.

#### Content Added by Release Year
Tracks content growth and release trends between 2010 and 2025.

---

## Dataset Information

The dataset contains information related to Netflix content including:

- Title
- Type
- Genre
- Country
- Language
- IMDb Rating
- Popularity
- Release Year
- Duration
- Cast
- Director

---

## Data Cleaning & Transformation

The following preprocessing steps were performed:

- Removed duplicate records
- Handled missing values
- Standardized text fields
- Transformed data types
- Created calculated columns
- Built data model relationships
- Created DAX measures for KPIs

---

## DAX Measures

### Total Contents

```DAX
Total Contents =
COUNTROWS(Netflix)
```

### Total Movies

```DAX
Total Movies =
CALCULATE(
    COUNTROWS(Netflix),
    Netflix[Type] = "Movie"
)
```

### Total TV Shows

```DAX
Total TV Shows =
CALCULATE(
    COUNTROWS(Netflix),
    Netflix[Type] = "TV Show"
)
```

### Total Countries

```DAX
Total Countries =
DISTINCTCOUNT(Netflix[Country])
```

### Total Languages

```DAX
Total Languages =
DISTINCTCOUNT(Netflix[Language])
```

---

## Key Insights

### Content Distribution

- Movies represent approximately 52% of the catalog.
- TV Shows represent approximately 48% of the catalog.

### Country Analysis

- United States contributes the highest number of titles.
- United Kingdom, Japan, China, and South Korea are among the top content-producing countries.

### Genre Analysis

- Drama is the most dominant genre.
- Comedy and Animation are also highly represented.

### Language Analysis

- English is the most common language.
- Japanese, Korean, Chinese, French, and Spanish are widely available.

### Ratings Analysis

- Most content falls within the IMDb rating range of 6–8.
- High-rated content significantly outnumbers low-rated titles.

### Growth Trends

- Netflix experienced substantial content growth from 2010 onward.
- Content additions remained consistently high through recent years.

---

## Tools & Technologies

| Category | Technology |
|------------|------------|
| Visualization | Power BI |
| Data Transformation | Power Query |
| Calculations | DAX |
| Data Analysis | Business Intelligence |
| Version Control | Git |
| Repository Hosting | GitHub |

---

## Project Structure

```text
netflix-content-analysis-dashboard
│
├── Dataset
│   └── netflix_dataset.csv
│
├── Dashboard
│   └── Netflix_Content_Analysis.pbix
│
├── Images
│   └── dashboard-overview.png
│
├── Documentation
│   └── Project_Report.pdf
│
├── README.md
├── LICENSE
└── .gitignore
```

---

## Business Impact

This dashboard helps stakeholders:

- Understand Netflix content distribution.
- Monitor content growth trends.
- Analyze genre popularity.
- Evaluate language diversity.
- Identify top-performing content categories.
- Support data-driven content strategy decisions.

---

## Future Enhancements

- Real-time Netflix data integration
- Recommendation system analytics
- Viewer engagement analysis
- Machine learning forecasting
- Sentiment analysis of reviews
- Regional content performance tracking

---

## Author

**Your Name**

Data Analyst | Power BI Developer | Business Intelligence Enthusiast

GitHub: https://github.com/yourusername

LinkedIn: https://linkedin.com/in/yourprofile

---

## License

This project is licensed under the MIT License.

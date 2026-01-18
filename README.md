# Arogya Healthcare Analytics

## Overview
The **Arogya Healthcare Analytics** project provides an advanced analysis of hospital-level healthcare data across India, focusing on **quality, access, and patient engagement patterns**.  
Using Python (NumPy, Pandas, Matplotlib, Seaborn), the project delivers **actionable insights, feature engineering, and rich visual storytelling** for data-driven healthcare planning.


## Objective
- Identify **state and district-level disparities** in hospital quality.
- Analyze **hospital performance** based on ratings and patient feedback.
- Detect **high-density regions under capacity stress**.
- Engineer features to quantify **patient engagement reliability**.
- Present **actionable insights** for healthcare improvement and policy decisions.


## Dataset
- File: `arogya_healthcare_india.csv`  
- Source: Hospital-level structured healthcare data  
- Columns:id                 2566 non-null   object 
 1   City               2566 non-null   object 
 2   State              2566 non-null   object 
 3   District           2566 non-null   object 
 4   Density            2566 non-null   float64
 5   Latitude           2566 non-null   float64
 6   Longitude          2566 non-null   float64
 7   Rating             2566 non-null   float64
 8   Number of Reviews  2566 non-null   int64  
dtypes: float64(4), int64(1), object(4)


## Tech Stack
- **Python 3**  
- **Pandas** – Data manipulation & cleaning  
- **NumPy** – Statistical analysis & feature engineering  
- **Matplotlib** – Static visualizations  
- **Seaborn** – Advanced visualizations & statistical plots  
- **Google Colab** – Cloud-based notebook environment  


## Project Steps

### 1. Data Loading & Audit
- Loaded CSV dataset into Pandas dataframe.
- Checked for missing values, data types, and data consistency.
- Calculated descriptive statistics (mean, median, std, IQR) using **NumPy**.
- Detected outliers in hospital ratings.

### 2. Feature Engineering
- **Engagement Score** = `log(1 + number_of_reviews) * rating`  
  Quantifies patient feedback reliability and volume.
- **Density Band** – Categorized hospitals into quartiles (Low, Medium, High, Very High) for density-based analysis.

### 3. Data Analysis & Visualization
- **Distribution Analysis** – Histogram of hospital ratings with KDE.
- **Density vs Ratings** – Boxplots highlighting capacity stress.
- **Patient Engagement** – Violin plots and scatterplots for engagement insights.
- **City-Level Quality vs Volume** – Scatterplots to identify top-performing cities.
- **State-Level Ratings** – Horizontal bar chart to compare states.
- **Correlation Analysis** – Heatmap for density, ratings, reviews, and engagement score.

### 4. Insights
- High-density districts show **lower rating stability**, indicating capacity stress.
- Hospitals with **higher engagement** (more reviews) display **more stable ratings**.
- Metro cities have high patient volume but **not necessarily higher quality**.
- Engagement score identifies hospitals that may **require operational focus or policy intervention**.


## Visuals
All visualizations are stored in the `/visuals` folder:
- `rating_distribution.png` – Distribution of hospital ratings
- `density_vs_rating.png` – Boxplot of ratings across density bands
- `engagement_violin.png` – Engagement score distribution
- `city_rating_scatter.png` – City-level rating vs total reviews
- `correlation_heatmap.png` – Feature correlation heatmap


## How to Use
1. Clone the repository:
```bash
git clone https://github.com/<preetam-katolkar>/arogya-healthcare-analytics.git

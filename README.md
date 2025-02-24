# Machine-Learning-Based-Analaysis-of-Movie-Success


This repository contains the code and analysis from a project report that investigates the factors contributing to the commercial and artistic success of movies. Using historical IMDb data from 2006 to 2016, the project leverages machine learning techniques—including Random Forest classifiers and A/B testing—to predict movie performance based on pre-release information. 

[View the Analysis Notebook](./Movie_Success_Analysis_Code.ipynb)

[View the Analysis Report](./Movie_Success_Analysis_report.pdf)


## Overview
This project examines historical trends in movies using IMDb data. The main goals are to:
- Identify key factors that drive commercial and artistic success.
- Develop predictive models using pre-release data (e.g., genres, actors, directors, runtime, release year).
- Explore the impact of runtime on revenue and ratings through A/B testing.
- Analyze genre differences in terms of competition and rating distributions.

## Dataset
The analysis is based on the top 1000 IMDb movies (2006–2016) obtained from Kaggle. The dataset includes:
- **Numeric Variables:** Rank, Year, Runtime (Minutes), Ratings, Revenues (Millions), Votes, Metascores.
- **Non-numeric Variables:** Title, Genre, Description, Directors, and Actors.

## Methodology

### Data Preprocessing
- **Cleaning:** Removed rows with missing values to retain 838 movies.
- **Transformation:** Converted categorical fields into numerical metrics based on historical revenue and vote data.

### Feature Engineering
- Derived new features to quantify “star power” for actors and directors.
- Incorporated runtime and release year as additional predictors.

### Modeling
- **Commercial Success Prediction:** A Random Forest classifier was developed to predict movie success (based on box office revenue and number of votes), achieving an accuracy of 82.1%.
- **Artistic Rating Prediction:** Another Random Forest model predicted artistic ratings (using user ratings and metascores) with an accuracy of 62.3%.

### A/B Testing
- Investigated the impact of runtime by classifying movies as “Feature” (runtime > 120 minutes) or “Non-Feature.”
- Statistical tests (z-score, p-value, and confidence intervals) indicated that feature movies perform significantly better in both revenue and rating.

### Genre Analysis
- Explored differences in movie performance across genres.
- Found that genres with fewer movies (e.g., Horror and Romance) may have an advantage due to lower competition, despite generally lower ratings compared to more populous genres like Adventure, Drama, and Action.

## Results
- **Commercial Success:** Predictive model accuracy of 82.1%.
- **Artistic Success:** Predictive model accuracy of 62.3%.
- **Runtime Impact:** A/B testing confirmed that movies longer than 120 minutes tend to be more successful both commercially and artistically.
- **Genre Insights:** Analysis suggests that genre competition and scarcity can significantly affect a movie’s chance of success.

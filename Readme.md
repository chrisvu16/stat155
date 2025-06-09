# Salary Prediction in the Technology Sector

## Research Question

This project explores the question: What factors influence salary levels in the tech industry, and how accurately can we predict them? Tech is growing rapidly, especially with the rise of fields like data science, artificial intelligence, and machine learning. As the industry evolves, it’s important for people entering the field to understand what kind of compensation they should expect. Whether someone’s aiming for a remote role at a startup or a senior position at a large company, having insight into salary trends can help them make more confident career decisions.

The goal of this study is to examine how different variables such as job title, experience level, company size, remote work flexibility, and employment type impact salaries across various tech roles. I’ll start with exploratory data analysis to understand the structure of the dataset and uncover any patterns or trends. Then the next step is to build a model to predict salary outcomes based on these features. I'm guessing that roles focused on AI and data will be among the highest paid and that seniority and remote work will also play big roles in determining compensation.

## Dataset

The dataset I will be exploring contains salary information from professionals in the tech industry, collected through the website aijobs.net. This site allows individuals to submit their job and salary information in a survey-style format, and the dataset is continuously updated. The dataset includes over 100,000 entries and 11 features. Each entry represents a single worker’s information for a given year and includes variables such as job title, experience level, salary, etc.

## 📁 Project Structure

This repository contains a multi-part analysis pipeline focused on salary prediction using simulated and real-world data.

### 🔧 Tools Used

-   **RStudio**\
-   **R version**: 4.4.1\
-   **Quarto**: for rendering `.qmd` files\
-   **Packages/Libraries**:
    -   `tidyverse`
    -   `ggthemes`
    -   `maps`
    -   `countrycode`
    -   `scales`
    -   `dplyr`
    -   `lightgbm`

``` r
install.packages(c("tidyverse", "ggthemes", "maps", "countrycode", "scales", "dplyr","lightgbm"))
```

### 📂 Folder Descriptions

-   **Project1/**
    -   `salaries.csv`: The raw dataset used in this analysis.\
    -   `Readme.md`: Markdown file detailing the dataset columns and structure.
-   **Project2/**
    -   `eda.qmd`: Quarto file performing exploratory data analysis (EDA) on the dataset, including visualizations and summary statistics.
-   **Project3/**
    -   `model.qmd`: Quarto file that builds and evaluates a predictive model on the salary data using LightGBM.
-   **Project4/**
    -   `Monte_Carlo_Sim.qmd`: Monte Carlo simulation script that evaluates model performance across different LightGBM hyperparameter combinations.

\

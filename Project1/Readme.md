# Salary Prediction in the Technology Sector

## Research Question

This project explores the question: What factors influence salary levels in the tech industry, and how accurately can we predict them? Tech is growing rapidly, especially with the rise of fields like data science, artificial intelligence, and machine learning. As the industry evolves, it’s important for people entering the field to understand what kind of compensation they should expect. Whether someone’s aiming for a remote role at a startup or a senior position at a large company, having insight into salary trends can help them make more confident career decisions.

The goal of this study is to examine how different variables such as job title, experience level, company size, remote work flexibility, and employment type impact salaries across various tech roles. I’ll start with exploratory data analysis to understand the structure of the dataset and uncover any patterns or trends. Then the next step is to build a model to predict salary outcomes based on these features. I’m guessing that roles focused on AI and data will be among the highest paid and that seniority and remote work will also play big roles in determining compensation.

## Dataset

The dataset I will be exploring contains salary information from professionals in the tech industry, collected through the website aijobs.net. This site allows individuals to submit their job and salary information in a survey-style format, and the dataset is continuously updated. The data is already in a csv file, so I just downloaded the raw csv file. The dataset includes over 100,000 entries and 11 features. Each entry represents a single worker’s information for a given year and includes variables such as job title, experience level, salary, etc.

-   **Observations:** 104,104
-   **Features:** 11

### Data Summary

-   **work_year:** The year the salary was paid.
-   **experience_level:** The experience level in the job during the year:<br>EN – Entry-level / Junior<br>MI – Mid-level / Intermediate<br>SE – Senior-level / Expert<br>EX – Executive-level / Director
-   **employment_type:** The type of employment:<br>PT – Part-time<br>FT – Full-time<br>CT – Contract<br>FL – Freelance
-   **job_title:** The role worked during the year.
-   **salary:** The total gross salary amount paid.
-   **salary_currency:** The currency of the salary paid.
-   **salary_in_usd:** The salary in USD (FX rate divided by avg. USD rate of the respective year).
-   **employee_residence:** Employee’s primary country of residence in during the work year.
-   **remote_ratio:** The overall amount of work done remotely, possible values are as follows:<br>0 – No remote work (less than 20%) <br>50 – Partially remote/hybrid<br>100 – Fully remote (more than 80%)
-   **company_location:** The country of the employer’s main office or contracting branch.
-   **company_size:** The average number of people that worked for the company during the year: <br>S – Small (\< 50 employees)<br>M – Medium (50–250)<br>L – Large (\> 250)

``` r
library(dplyr)
salary = read.csv("data/salaries.csv")
glimpse(salary)
```

```         
Rows: 104,104
Columns: 11
$ work_year          <int> 2025, 2025, 2025, 2025, 2025, 2025, 2025, 2025, 202…
$ experience_level   <chr> "SE", "SE", "SE", "SE", "MI", "MI", "MI", "MI", "SE…
$ employment_type    <chr> "FT", "FT", "FT", "FT", "FT", "FT", "FT", "FT", "FT…
$ job_title          <chr> "Big Data Engineer", "LLM Engineer", "Software Engi…
$ salary             <int> 110000, 80000, 240000, 170000, 140000, 120000, 2080…
$ salary_currency    <chr> "CAD", "EUR", "USD", "USD", "USD", "USD", "USD", "U…
$ salary_in_usd      <int> 78571, 84210, 240000, 170000, 140000, 120000, 20800…
$ employee_residence <chr> "CA", "DE", "US", "US", "US", "US", "US", "US", "US…
$ remote_ratio       <int> 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0…
$ company_location   <chr> "CA", "DE", "US", "US", "US", "US", "US", "US", "US…
$ company_size       <chr> "L", "L", "M", "M", "M", "M", "M", "M", "M", "M", "…
```

#  Data Professional Survey Analysis — Power BI

An interactive **Power BI dashboard** built to analyze data careers, salaries, skills, career transitions, and job satisfaction.

---

##  Project Objective

The objective of this project is to explore the professional landscape of people working in or entering the data field and identify patterns in:

- Job roles
- Salaries
- Programming languages
- Career transitions
- Education
- Job preferences
- Job satisfaction

The dashboard transforms survey data into an interactive analytical report using Microsoft Power BI.

---

##  Tools & Technologies

- **Microsoft Power BI** — Dashboard development and visualization
- **Power Query** — Data cleaning and transformation
- **DAX** — Measures and calculations
- **Excel** — Source dataset
- **GitHub** — Project version control and portfolio presentation

---

#  Home Page

The Home page acts as the landing page for the report and provides navigation to the main analytical sections.

### Navigation

-  Dashboard
-  Salary & Job Analysis
-  Skills & Career Analysis
-  Job Satisfaction Analysis

![Home Page](/images/Project4_Homepage.png)

---

#  Dashboard / Overview

The Dashboard provides a high-level overview of the survey.

### KPIs

- **Total Respondents**
- **Average Age of Survey Takers**
- **Average Estimated Salary**
- **Most Common Job Title**

### Visualizations

- Respondents by Job Title
- Salary Distribution
- Most Popular Programming Languages
- Career Switch into Data

### Interactive Slicers

- Country
- Job Title
- Switched Career?

![Dashboard Overview](/images/Project4_Page1.png)

---

#  Salary & Job Analysis

This page analyzes estimated salary and respondent distribution across different job roles, countries, and industries.

### Visualizations

- Highest Estimated Salaries by Data Role
- Respondents by Country
- Respondents by Industry
- Salary Distribution by Job Title
- Average Estimated Salary by Industry
- Average Estimated Salary by Country

![Salary & Job Analysis](/images/Project4_Page2.png)

---

#  Skills & Career Analysis

This page focuses on career transitions, education, and factors influencing career decisions.

### Visualizations

- Difficulty Getting into Data
- Education Level of Respondents
- Age Distribution of People Who Switched into Data
- Most Desired Job Factors

![Skills & Career Analysis](/images/Project4_Page3.png)

---

# 😊 Job Satisfaction Analysis

This page analyzes satisfaction across different workplace factors.

### Satisfaction Factors

- Salary
- Work/Life Balance
- Coworkers
- Management
- Upward Mobility
- Learning New Things

### Visualizations

- Average Satisfaction by Factor
- Satisfaction by Job Role
- Overall Satisfaction Distribution
- Satisfaction Ratings by Factor
- Happiness with Salary
- Happiness with Work/Life Balance

![Job Satisfaction Analysis](/images/Project4_Page4.png)

---

#  Data Preparation

The dataset was cleaned and transformed using **Power Query**.

### Main Transformations

- Removed unnecessary columns
- Kept relevant survey questions
- Renamed columns for readability
- Checked and corrected data types
- Cleaned salary ranges
- Split salary ranges into minimum and maximum values
- Created `Salary Min (K)`
- Created `Salary Max (K)`
- Created `Salary Midpoint (K)`
- Unpivoted satisfaction columns
- Created `Satisfaction Factor`
- Created `Satisfaction Rating`
- Created `Satisfaction Level`

---

##  Salary Transformation

The original salary column contained salary ranges such as:

```text
0-40k
41k-65k
66k-85k
86k-105k
106k-125k
125k-150k
150k-225k
225k+

The salary range was transformed into:

- `Salary Min (K)`
- `Salary Max (K)`
- `Salary Midpoint (K)`

### Salary Midpoint

For ranges with both minimum and maximum values:

```text
Salary Midpoint = (Salary Min + Salary Max) / 2
```

For open-ended ranges such as:

```text
225k+
```

the midpoint remains blank because there is no upper salary limit.

> **Note:** Salary Midpoint represents an estimated salary based on the selected salary range. It is not the respondent's exact salary.

---

#  Satisfaction Data Transformation

The six satisfaction columns were unpivoted in Power Query.

This created:

```text
Satisfaction Factor
Satisfaction Rating
```

A `Satisfaction Level` column was then created using the following classification:

```text
0–4  → Dissatisfied
5–7  → Neutral
8–10 → Satisfied
```

This transformation allowed all satisfaction factors to be analyzed consistently.

---

#  DAX Measures

The dashboard uses DAX measures for KPI calculations and analysis.

### Total Respondents

```DAX
Total Respondents =
DISTINCTCOUNT('Data Professional Survey'[Unique ID])
```

### Average Estimated Salary

```DAX
Average Estimated Salary =
AVERAGE('Data Professional Survey'[Salary Midpoint (K)])
```

### Average Age

```DAX
Average Age =
AVERAGE('Data Professional Survey'[Q10 - How old are you?])
```

---

#  Dashboard Highlights

The current dashboard includes:

| Metric | Value |
|---|---:|
| Total Respondents | **3.722K** |
| Average Age | **29.87** |
| Average Estimated Salary | **54.15K** |
| Most Common Job Title | **Data Analyst** |
| Most Popular Programming Language | **Python** |

---

#  Key Insights

### 1. Data Analyst is the most represented role

Data Analyst is the most common job title among respondents.

### 2. Python is the most popular programming language

Python has the highest number of respondents among the programming languages shown in the dashboard.

### 3. Salary varies across data roles

The estimated salary analysis shows noticeable differences between data-related job roles.

### 4. Better Salary is the most desired job factor

Better Salary has the highest number of responses among the job factors analyzed.

### 5. Career transition into data

The dashboard shows the proportion of respondents who entered the data field from another career.

### 6. Job satisfaction varies by workplace factor

Satisfaction differs across salary, work/life balance, coworkers, management, upward mobility, and learning opportunities.

---

#  Interactivity

The report includes interactive slicers:

-  Country
-  Job Title
-  Career Switch

The slicers are synchronized across relevant analytical pages.

The **Dashboard / Overview** page acts as the main filtering and control page.

---

#  Navigation

The report includes navigation buttons to move between pages.

```text
                        HOME
                          │
                          ▼
                     DASHBOARD
                     /    |     \
                    /     |      \
                   ▼      ▼       ▼
              Salary   Skills     Job
               & Job    & Career  Satisfaction
```

Navigation features include:

- Home button
- Dashboard button
- Back navigation
- Next-page navigation
- Clear All Slicers button

---

#  Calculation Notes

`Unique ID` is generally aggregated using **Distinct Count** when measuring respondents.

This prevents the same respondent from being counted multiple times.

For example:

```text
Unique ID → Distinct Count
```

is used for respondent-based visuals.

After unpivoting the satisfaction columns, each respondent can have multiple satisfaction records. Therefore, the aggregation used for satisfaction visuals depends on what the visual is measuring.

---

#  Project Structure

```text
Power-BI/
│
├── DAX/
├── images/
├── Power Query/
├── Project_1/
├── Project_2/
├── Project_3/
│
└── Project_4/
    ├── Data Professional Survey.pbix
    ├── Data Professional Survey.pdf
    ├── Power BI - Final Project.xlsx
    └── README.md
```

---


#  Future Improvements

Potential future improvements include:

- Advanced DAX measures
- Drill-through pages
- Report tooltips
- Dynamic titles based on slicer selections
- Additional segmentation
- More advanced Power BI interactions
- Further dashboard theme refinement
- Publishing the report to Power BI Service

---

#  Project Information

**Project:** Data Professional Survey Analysis

**Platform:** Microsoft Power BI

**Focus:**  
Data Analytics • Business Intelligence • Data Careers • Salary Analysis • Job Satisfaction

---

##  Project Workflow

```text
Raw Survey Data
       ↓
Power Query Cleaning
       ↓
Data Transformation
       ↓
DAX Measures
       ↓
Exploratory Analysis
       ↓
Power BI Visualizations
       ↓
Interactive Slicers
       ↓
Page Navigation
       ↓
Final Dashboard
```

---

##  Final Report

The final report combines:

**Careers + Salaries + Skills + Job Satisfaction**

into an interactive Power BI dashboard designed for data analysis, visualization, and portfolio presentation.
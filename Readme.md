### 🧠 Built With

- [Quarto (.qmd)](https://quarto.org/)
- Language: **R**

![R](https://img.shields.io/badge/Language-R-blue.svg)

# 🤖 AI & Automation Employment Analysis

This Quarto project explores how Artificial Intelligence and automation are reshaping employment, wages, and skill requirements across industries. It answers three core questions with data-driven analysis and compelling visuals.

---

## ❓ Core Questions Addressed

1. **Is AI taking away jobs in different industries?**
2. **How has automation affected wage inequality across different sectors?**
3. **Which skills are most valuable in an AI-powered future workforce?**

---

## 🎯 Project Goals

This analysis investigates:
- Employment trends across U.S. industries (2023–2033)
- The role of AI adoption in job creation or loss
- Wage patterns from 2014–2023 in relation to automation risk
- Skill demand trends using job posting data

---

## 📦 Data Sources

- **Employment Projections**: Bureau of Labor Statistics (BLS) — `industry.xlsx`
- **Wage Data**: BLS Occupational Employment & Wage Statistics (scraped via `rvest`)
- **Skill Demand**: Online job postings (via text scraping)

---

## 🛠 Tools & Libraries

The project uses **R** and **Quarto** with the following libraries:

```r
tidyverse     # Data wrangling and visualization
readxl        # Excel import
rvest         # Web scraping (for wage and skill data)
ggrepel       # Labeling on ggplots
httr          # User-agent setup for scraping
scales        # Format axes and values in plots

## 🧪 Methodology Overview

### Question 1: 📉 Job Loss or Gain?
- Join AI adoption data with industry job projections  
- Create a custom **Automation Risk Score**:  
  `Automation Risk Score = AI Adoption × (–% Employment Change)`  
- Visualize sectors that are growing **despite** high automation

### Question 2: 💸 Wage Inequality?
- Scrape historical wage tables (2014–2023)
- Compare wage changes by automation exposure
- Highlight how automation affects **low-, mid-, and high-wage** roles

### Question 3: 🧠 Skills of the Future?
- Analyze job ads and extract keywords
- Rank skill frequency by industry and job type
- Identify **top-growing competencies** in the AI economy

---

## 📊 Key Findings

- **AI doesn’t always mean job loss** – sectors like Healthcare are growing even with rising automation
- **Retail is shrinking** even with **lower AI adoption**, likely due to e-commerce
- **Wage growth diverges** across sectors, with **low-wage jobs stagnating** under automation pressure
- **Soft skills + Tech skills** are in highest demand in the AI-driven job market

---

## ▶️ How to Run

1. **Install the necessary libraries**:

```r
install.packages("tidyverse")
install.packages("rvest")
install.packages("readxl")
install.packages("ggrepel")
install.packages("httr")
2. Ensure industry.xlsx is in the project folder.

3. Open AI_Automation_Employement_Analysis.qmd in RStudio or VS Code with Quarto.

4. Render the document

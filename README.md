# 💼 Top Paying AI Jobs in 2025: Exploratory Data Analysis

An exploratory data analysis of the global AI job market. The project examines how salaries relate to experience, job title, location, company size, remote work, and required skills, to deliver data-driven insights for job seekers, recruiters, and industry analysts.

## Highlights

- Analysis of 30,000 AI job postings from 2024 and 2025 across 20 countries
- Salary breakdowns by experience level, company size, work arrangement, country, and skill
- Interactive world map of average AI salaries (Plotly)
- Skill-by-country salary heatmaps, including a focused view of the United States

## Dataset

Two CSV files (`ai_job_dataset.csv` and `ai_job_dataset1.csv`) are combined into a single DataFrame of 30,000 postings and 20 columns, including:

| Group | Columns |
|-------|---------|
| Role | `job_title`, `experience_level` (EN, MI, SE, EX), `employment_type`, `years_experience`, `industry` |
| Compensation | `salary_usd`, `salary_currency`, `salary_local`, `benefits_score` |
| Location and work model | `company_location`, `employee_residence`, `remote_ratio` (0, 50, 100), `company_size` |
| Requirements | `required_skills`, `education_required` |
| Posting details | `job_id`, `company_name`, `posting_date`, `application_deadline`, `job_description_length` |

The data has no missing values except `salary_local`, which is only filled for half of the rows. All salary analysis uses the standardized `salary_usd` column.

## Analysis

1. **Data overview:** shape, data types, missing values, summary statistics, and a correlation heatmap.
2. **Salary distribution:** histogram and boxplot of `salary_usd`.
3. **Job market structure:** most common job titles, top hiring countries, share of jobs by country, and the distribution of experience levels and work types.
4. **Salary drivers:**
   - Salary by experience level, company size, and remote ratio.
   - Highest-paying job titles and countries (bar charts and a choropleth map).
5. **Skills analysis:**
   - Split and exploded the `required_skills` column to analyze each skill individually.
   - Highest-paying skills, and average salary by skill and country as a heatmap.
   - A dedicated skill-salary view for the United States.

## Key Findings

| Metric | Value |
|--------|-------|
| Postings analyzed | 30,000 |
| Mean salary | $118,670 |
| Median salary | $103,207 |
| Salary range | $16,621 to $410,273 |

- **Experience matters most.** Years of experience has a strong positive correlation with salary (0.74), far stronger than any other numeric variable.
- **Remote work barely affects pay.** Average salaries are very close across onsite ($117,824), hybrid ($119,014), and fully remote ($119,180) roles, and the three work types are split almost evenly (about one third each).
- **Location drives large differences.** The highest average salaries by company location are in Switzerland ($171,872), Denmark ($162,170), Norway ($160,273), and the United States ($144,326), while India ($64,455) and China ($71,119) are the lowest.
- **Top 10 countries by average salary:** Switzerland, Denmark, Norway, United States, United Kingdom, Netherlands, Singapore, Sweden, Germany, and Australia.

The remote work split is unusually even, so the dataset may be partly synthetic, and the findings are best treated as illustrative rather than exact market statistics.

## Tech Stack

- Python
- pandas, NumPy
- matplotlib, seaborn
- Plotly

## Getting Started

```bash
git clone <your-repo-url>
cd <your-repo-folder>
pip install pandas numpy matplotlib seaborn plotly
```

Place `ai_job_dataset.csv` and `ai_job_dataset1.csv` in the project root, then run:

```bash
jupyter notebook AiJobsEDA.ipynb
```

## Project Structure

```
.
├── AiJobsEDA.ipynb         # Full exploratory analysis
├── ai_job_dataset.csv      # Dataset part 1 (not included)
├── ai_job_dataset1.csv     # Dataset part 2 (not included)
└── README.md
```

## Author

Furkan

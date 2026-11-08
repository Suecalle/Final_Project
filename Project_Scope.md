# Project Scope: The AI Engineer Job Market

## 1. Project Goals
**Main question:** How do AI/ML engineer roles compare with other data and software roles in salary, experience level and remote work, globally and in the UK?

**Sub-questions**
1. How do salaries for AI Engineer and Machine Learning Engineer compare with Data Scientist, Data Engineer, Data Analyst and Software Engineer?
2. How does salary change with experience level (EN, MI, SE, EX) for each role?
3. How common is remote work, and does it relate to salary?
4. How does the UK compare with the US for the same roles?

**Audience:** Hiring managers and recruiters reviewing my portfolio, and people considering a move into AI engineering.

## 2. Data
- **Source:** aijobs.net Global AI, ML, Data Science Salary Index (`salaries.csv`), from https://github.com/foorilla/ai-jobs-net-salaries (CC0-1.0)
- **Raw size:** 151,445 rows x 11 columns
- **After cleaning:** 79,532 duplicate rows removed, leaving 71,913 rows
- **Subset used:** six job titles (Machine Learning Engineer, AI Engineer, Data Scientist, Data Engineer, Data Analyst, Software Engineer), full-time roles only: 29,819 rows
- **Salary column:** `salary_in_usd`, so all currencies are comparable
- **Missing values:** none

**Known limitations**
- Self-reported anonymous survey data, so it may not represent the whole market
- Mostly US data; the UK sample is small (1,269 rows, only 38 AI Engineers)
- Experience levels are unbalanced (senior and mid-level dominate; executive is rare)
- The data has no ID column, so removed duplicates may sometimes have been genuine separate entries
- Hybrid roles are too few (154 rows) to analyse

## 3. Analysis Plan (completed)
1. **Clean:** removed duplicates, checked missing values and data types
2. **Filter:** six job titles, full-time roles only
3. **Summarise:** count, median and mean salary by job title, globally and for the UK
4. **Isolate variables:** salary by experience level and by remote ratio (group medians)
5. **Compare:** job title vs salary, experience level vs salary, US vs UK
6. **Visualise:** three charts (median salary by job title, by experience level and title, US vs UK)

## 4. Evaluation
- Sample sizes are reported next to results, and small groups are flagged
- Medians are used alongside means, because a few high salaries pull the means up
- Results are described as associations, not causes

## 5. Output
- `Final_Project.ipynb`: analysis with Markdown notes after each step
- Three charts saved as PNG files
- `readme.md`: summary, key findings, data source and limitations
- Written conclusions at the end of the notebook

## 6. Changes from the Original Plan
- Compared AI/ML roles against other job titles with simple filtering, after dropping a more complex grouping approach.
- Compared the US with the UK, not the UK with "global", because the global figure already includes the UK.
- Skipped splitting UK results by experience level, because the UK sample is too small.
- Used group medians instead of correlations to show relationships between variables.
- Limited the remote work analysis to summary figures because of the small hybrid group.
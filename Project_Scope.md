# Project Scope: The AI Engineer Job Market

## 1. Project Goals
**Main question:** How do AI/ML engineer roles compare with other data and
software roles in salary, experience level, and remote work, globally and in
the UK?

**Sub-questions**
1. How do salaries for AI Engineer and Machine Learning Engineer compare with
   Data Scientist, Data Engineer, Data Analyst, and Software Engineer?
2. How does salary change with experience level (EN, MI, SE, EX) for each role?
3. How common is remote work (remote_ratio) in AI roles compared with the
   other roles?
4. How does the UK compare with the global/US picture for AI roles?

**Audience:** Hiring managers and recruiters reviewing my portfolio, and
people considering a move into AI engineering.

## 2. Data
- **Source:** aijobs.net salaries dataset (`salaries.csv`, GitHub snapshot)
- **Size:** 151,445 rows × 11 columns
- **Key columns:** work_year, experience_level, employment_type, job_title,
  salary_in_usd, employee_residence, remote_ratio, company_location,
  company_size
- **Subset used:** six job titles (Machine Learning Engineer, AI Engineer,
  Data Scientist, Data Engineer, Data Analyst, Software Engineer),
  giving 76,730 rows
- **Salary column:** `salary_in_usd`, so all currencies are comparable

**Known limitations**
- Self-reported or crowdsourced data, so it may not represent the whole market
- Probably heavily US-weighted, so the UK sample may be small
- Experience levels are unbalanced (SE and MI dominate; EX is rare)
- Some rows look duplicated (e.g. identical Manager salaries repeated), so I
  will check for and handle duplicates
- AI Engineer has far fewer rows (2,013) than the other titles, so
  comparisons need care

## 3. Analysis Plan
1. **Clean:** check missing values and duplicates; confirm data types
2. **Filter:** keep the six selected titles
3. **Summarise:** count, mean, and median `salary_in_usd` by job title
   (median matters because salaries are skewed)
4. **Isolate variables:** salary by experience level; salary by remote_ratio
5. **Compare two variables:** job title vs. salary, and experience level vs.
   salary, to look for a relationship
6. **UK vs. global:** filter `company_location == "GB"` and repeat the key
   comparisons
7. **Visualise:** bar chart of median salary by title, box plot of salary by
   experience level, bar chart of remote ratio by title

## 4. Evaluation
- Report sample sizes next to every result, and flag groups that are too small
  to trust
- Use medians as well as means so outliers don't distort the story
- Be explicit that this shows correlation in a snapshot, not causes
- If a step turns out to be a dead end (e.g. too little UK data), adjust the
  scope and note why

## 5. Output
- Final Jupyter notebook (`Final_Project.ipynb`) with clear markdown
  explanations between code cells
- 3–4 clean visualisations
- A short written conclusion answering the main question
- `readme.md` on GitHub summarising the project, data source, and findings


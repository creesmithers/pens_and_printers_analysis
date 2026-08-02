# Pens and Printers Revenue Analysis
**Note:** This project was completed as part of a DataCamp Data Analyst Certification course. My more recent projects reflect my current technical skill, please see the pinned repositories on my GitHub profile.

## Overview
This project cleans and validates data to help with analysis. The goal was to understand drivers of revenue and what ad campaigns to prioritize between calls, emails, or both.  

## Tools
Python, Pandas, Seaborn, scipy.stats, NumPy, PowerBI

## Dataset
The dataset contains predictors such as week, sales_method, customer_id, number sold, revenue, years_as_customer, number site visits, and state

## Methods
- Missing data: Identified missing revenue values and imputed them using the median revenue within each sales_method group (rather than a single global median), since revenue varies substantially by contact method and a group-level median preserves that structure instead of flattening it.
- Data quality check: Found no repeat customer_id values in the dataset. Flagged this for follow-up rather than treating it as ground truth — it's unclear whether this reflects genuinely one-time purchase behavior or a data entry/tracking issue upstream, and that ambiguity should be resolved before the finding is used to drive a business decision 
- Statistical Testing: Ran a one-way ANOVA testing to identify differences in revenue by customer contact methods

## Results
Found there to be a statistically significant difference in average revenue by contact method. Contact by combination of email + call was higher than just call or email. 
Calculated business metric of total Revenue per Customer by Sales Method:
- Call: $47.65
- Email: $97.01
- Email + Call: $183.80

- Found Email only clients account for 84% of week 1 revenue
- Found 'Email + Call' strategy to account for 27% of revenue in week 3 but grew to 70% by last week
  

## Files
Product Sales (Pens and Printers).pptx   - Slide deck summarizing analysis, statistical findings, and business recommendations
pens_and_printers_notebook.ipynb         - Jupyter notebook containing data cleaning, exploratory data analysis, and statistical testing
pens_and_printers_visual.pbix            - PowerBI dashboard used to visualize revenue trends by contact method and week. 


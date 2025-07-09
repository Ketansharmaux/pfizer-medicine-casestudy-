# pfizer-medicine-casestudy-
Case Study: Pfizer’s Personalized Medicine Initiative
Case Study Background
Pfizer, one of the world's largest pharmaceutical companies, is leading the charge in developing personalized medicine, using data from clinical trials and genomics to discover new drugs tailored to individual patients. With the rise of precision medicine, Pfizer's R&D team is under pressure to analyze vast amounts of clinical trial data to determine which drug formulations work best for different groups of patients.
The key to success lies in harnessing this data effectively. This project is a pivotal part of their efforts to uncover insights from clinical trials and genomics data to create more effective and personalized treatment plans for patients. Your role as a data analyst is to dive deep into this dataset and help the stakeholders make critical decisions. The insights derived from this data will influence the future of personalized medicine at Pfizer.
Your goal is to analyze the provided dataset, find actionable insights, and present them in a way that non-technical stakeholders can easily understand and act upon. While machine learning is not required, the use of Excel and Looker Studio for data visualization and analysis is crucial to communicating insights effectively.

Problem Selection
The problem you need to solve is related to drug efficacy and patient response variability based on the genomics and clinical trial data provided. Pfizer is eager to understand:
Which patient demographics and genetic factors affect the efficacy of specific drugs?
Are there any patterns in the side effects experienced by patients across different demographics and genetic profiles?
Can we determine the most effective treatment plans based on the progression-free survival rates?
This analysis is crucial because discovering these patterns will help Pfizer tailor future treatments, improve clinical trial design, and reduce adverse side effects for specific patient groups.

Stakeholder Involvement
Internal Stakeholders: Pfizer's Research and Development (R&D) team, Data Science Team, and Clinical Researchers.
External Stakeholders: Medical professionals, regulatory bodies, and patients.
Dataset:
DACS19 - Pfizer’s Personalised Medicine.csv
Data Dictionary:
Column Name
Description
Patient_ID
Unique identifier for each patient.
Age
Age of the patient.
Gender
Gender of the patient (Male/Female/Other).
Ethnicity
Ethnicity of the patient.
Medical_History
Medical conditions such as Diabetes, Hypertension, etc.
Genomic_Profile
Summary of the patient's genomic mutations.
Trial_ID
Unique identifier for each clinical trial.
Drug_Name
Name of the drug administered.
Trial_Phase
The phase of the clinical trial (Phase I-IV).
Start_Date
Start date of the clinical trial.
End_Date
End date of the clinical trial.
Dose
Dose of the drug administered (in mg).
Adverse_Events
Adverse events or side effects were reported during the trial.
Treatment_ID
Unique identifier for each treatment cycle.
Dose_Administered
Actual dose administered to the patient (in mg).
Treatment_Outcome
Outcome of the treatment (Improved/No Change/Deteriorated).
Side_Effects
Side effects experienced by the patient during treatment.
Duration_of_Treatment
Duration for which the treatment was administered (in days).
Success_Indicator
1 for success, 0 for failure based on treatment outcome.
Gene_Name
Name of the gene being studied (BRCA1, TP53, etc.).
Mutation_Status
Mutation status of the gene (Positive/Negative).
Expression_Level
Expression level of the gene (numeric value).
Biomarker_Level
Biomarker level detected in the patient (numeric value).
Efficacy_Score
Efficacy score of the treatment based on patient response.
Survival_Rate
Survival rate post-treatment (in months).
Progression_Free_Survival
Time without disease progression after treatment (in months).


Data Preprocessing & Cleaning
Before diving into the analysis, it is critical to clean and preprocess the data for better quality. Steps include:
Handling Missing Data: Check for missing values, particularly in fields like Genomic_Profile, Adverse_Events, and Survival_Rate. Impute missing values or remove rows where critical data is unavailable.
Ensuring Data Consistency: Validate that the Dose_Administered matches the trial protocols and identify any outliers.
Categorical Encoding: For columns like Gender, Ethnicity, and Genomic_Profile, ensure proper labeling for clear analysis in Excel.
Date Format Validation: Ensure Start_Date and End_Date fields are correctly formatted and check the duration of clinical trials.
Check for Duplicates: Ensure no duplicate patient records or trial data exist.
Basic-Level Questions
Patient Distribution by Age Group
Question: Analyze the number of patients in each age group using a Pivot Table.
Hint: Place "Age" in the Rows field and "Patient_ID" in the Values field, summarizing "Patient_ID" as a count. Group ages into ranges (e.g., 18-30, 31-50, etc.).
How it Helps: Helps identify which age groups are participating more in clinical trials.
Impact: Provides insights for focusing clinical trials on age groups with the highest participation.
Drug Distribution by Trial Phase
Question: Analyze the distribution of different drugs across clinical trial phases using a Pivot Table.
Hint: Place "Trial_Phase" in the Rows field and "Drug_Name" in the Values field, summarizing "Drug_Name" as a count.
How it Helps: Understand which drugs are most advanced in the trial process.
Impact: Helps the R&D team prioritize resources toward drugs in later-phase trials.


Side Effects by Drug
Question: Analyze the number of side effects reported by drug using a Pivot Table.
Hint: Place "Drug_Name" in the Rows field and "Side_Effects" in the Values field, summarizing "Side_Effects" as a count.
How it Helps: Provides a clear view of which drugs have the most reported side effects.
Impact: Helps identify drugs that may need dosage adjustments or further testing to reduce side effects.

Patient Distribution by Ethnicity
Question: Analyze the number of patients in each ethnicity category using a Pivot Table.
Hint: Place "Ethnicity" in the Rows field and "Patient_ID" in the Values field, summarizing "Patient_ID" as a count.
How it Helps: Understands the diversity of participants in the clinical trials.
Impact: Ensures inclusivity and that clinical trials are representative of the general population.

Average Dose Administered by Drug
Question: Calculate the average dose administered for each drug.
Hint: Place "Drug_Name" in the Rows field and "Dose_Administered" in the Values field, summarizing "Dose_Administered" as an average.
How it Helps: Helps to identify standard dosing practices across trials.
Impact: Provides insights into optimizing dosages for better efficacy.

Efficacy Score by Drug and Age Group
Question: Analyze the average efficacy score by drug and age group.
Hint: Use "Drug_Name" and "Age" in the Rows field and "Efficacy_Score" in the Values field, summarizing "Efficacy_Score" as an average. Group ages into ranges (e.g., 18-30, 31-50).
How it Helps: Shows how different age groups respond to various drugs.
Impact: Helps develop targeted treatments for specific age demographics.

Progression-Free Survival by Mutation Status
Question: Analyze the average progression-free survival based on the mutation status of patients.
Hint: Place "Mutation_Status" in the Rows field and "Progression_Free_Survival" in the Values field, summarizing "Progression_Free_Survival" as an average.
How it Helps: Determines how genetic mutations impact survival rates.
Impact: Guides personalized medicine efforts based on genetic factors.

Survival Rate by Gender and Drug
Question: Analyze the average survival rate by gender and drug.
Hint: Place "Gender" and "Drug_Name" in the Rows field and "Survival_Rate" in the Values field, summarizing "Survival_Rate" as an average.
How it Helps: Identifies whether certain drugs perform better for specific genders.
Impact: Helps in tailoring treatments based on gender for improved outcomes.

Side Effects by Age Group and Treatment Outcome
Question: Analyze the number of side effects reported by age group and treatment outcome.
Hint: Use "Age" and "Treatment_Outcome" in the Rows field and "Side_Effects" in the Values field, summarizing "Side_Effects" as a count.
How it Helps: Understand how age and treatment success are related to side effects.
Impact: Helps optimize treatment plans to minimize side effects in different age groups.

Drug Efficacy by Gene Mutation
Question: Analyze the efficacy score based on the presence of different gene mutations.
Hint: Place "Gene_Name" in the Rows field and "Efficacy_Score" in the Values field, summarizing "Efficacy_Score" as an average.
How it Helps: Highlights which gene mutations respond better to certain treatments.
Impact: Improves treatment personalization by understanding the genetic response to drugs.

Success Rate Correlation with Dose Administered
Question: Analyze if there is a correlation between the dose administered and treatment success rate.
Hint: Use a Scatter Plot in Excel between "Dose_Administered" and "Success_Indicator".
How it Helps: Reveals if higher doses lead to better or worse outcomes.
Impact: Helps optimize dosage for future treatments based on success trends.

Gene Expression Level vs. Survival Rate
Question: Analyze the relationship between gene expression levels and survival rates.
Hint: Use "Gene_Name" and "Expression_Level" in the Rows field and "Survival_Rate" in the Values field, summarizing "Survival_Rate" as an average.
How it Helps: Identifies how gene expression affects the longevity of patients.
Impact: Guides further genomic research to improve patient survival.

Adverse Events by Progression-Free Survival
Question: Analyze the relationship between the number of adverse events and progression-free survival.
Hint: Use "Adverse_Events" in the Rows field and "Progression_Free_Survival" in the Values field, summarizing "Progression_Free_Survival" as an average.
How it Helps: Determines how side effects impact the effectiveness of treatment.
Impact: Helps to develop safer treatment protocols that minimize adverse events.

Treatment Duration Impact on Efficacy
Question: Analyze how the duration of treatment affects the efficacy score.
Hint: Place "Duration_of_Treatment" in the Rows field and "Efficacy_Score" in the Values field, summarizing "Efficacy_Score" as an average.
How it Helps: Identifies whether longer treatment durations yield better results.
Impact: Helps in optimizing treatment timelines for better outcomes.

Biomarker Levels vs. Treatment Outcome
Question: Analyze how biomarker levels affect the treatment outcome.
Hint: Use "Biomarker_Level" in the Rows field and "Success_Indicator" in the Values field, summarizing "Success_Indicator" as an average.
How it Helps: Shows the influence of biomarkers on treatment success.
Impact: Aids in tailoring treatments based on biomarker levels for better precision.



Medium-Level Questions
Drug Efficacy by Age Group and Gender
Question: Analyze the average efficacy score by age group and gender.
Hint: Place "Age" and "Gender" in the Rows field and "Efficacy_Score" in the Values field, summarizing "Efficacy_Score" as an average. Group ages into ranges (e.g., 18-30, 31-50).
How it Helps: Shows how different demographics respond to various drugs.
Business Impact: Helps in tailoring treatments based on patient demographics for improved drug efficacy and personalized treatment approaches.
Adverse Events by Drug and Mutation Status
Question: Analyze the number of adverse events reported for each drug based on the patients' mutation status.
Hint: Place "Drug_Name" and "Mutation_Status" in the Rows field and "Adverse_Events" in the Values field, summarizing "Adverse_Events" as a count.
How it Helps: Identifies which drugs lead to more adverse events based on genetic profiles.
Business Impact: Helps the company decide if drugs need further testing for safety and efficacy in specific genetic groups.
Progression-Free Survival by Drug and Treatment Outcome
Question: Analyze the average progression-free survival for each drug and treatment outcome.
Hint: Use "Drug_Name" and "Treatment_Outcome" in the Rows field and "Progression_Free_Survival" in the Values field, summarizing "Progression_Free_Survival" as an average.
How it Helps: Highlights which drugs have the best outcomes in terms of delaying disease progression.
Business Impact: Helps prioritize drugs with the best long-term outcomes for specific patient groups.
Correlation between Treatment Duration and Side Effects
Question: Analyze if there is a correlation between the duration of treatment and the number of side effects reported.
Hint: Use a Scatter Plot in Excel, placing "Duration_of_Treatment" on the X-axis and "Side_Effects" on the Y-axis.
How it Helps: Reveals whether longer treatments are more likely to result in side effects.
Business Impact: Helps in designing optimal treatment plans that minimize side effects while maintaining efficacy.
Survival Rate by Ethnicity and Drug
Question: Analyze the average survival rate by ethnicity and drug.
Hint: Use "Ethnicity" and "Drug_Name" in the Rows field and "Survival_Rate" in the Values field, summarizing "Survival_Rate" as an average.
How it Helps: Shows how different ethnic groups respond to specific drugs in terms of survival.
Business Impact: Provides insights into tailoring drug treatments for different ethnic groups, ensuring inclusivity and efficacy across diverse populations.
Gene Expression Level by Treatment Outcome
Question: Analyze the average gene expression level based on treatment outcomes.
Hint: Place "Gene_Name" and "Treatment_Outcome" in the Rows field and "Expression_Level" in the Values field, summarizing "Expression_Level" as an average.
How it Helps: Shows the impact of gene expression on the success or failure of treatments.
Business Impact: Aids in understanding the role of genetic expression in treatment efficacy, influencing future drug research.
Success Rate by Drug and Gender
Question: Analyze the success rate of treatments based on drug and gender.
Hint: Place "Drug_Name" and "Gender" in the Rows field and "Success_Indicator" in the Values field, summarizing "Success_Indicator" as an average.
How it Helps: Helps identify whether there is a difference in treatment success rates across different genders for specific drugs.
Business Impact: Provides Pfizer with insights for tailoring treatment plans by gender, which could improve overall treatment success rates.
Impact of Gene Mutation on Side Effects
Question: Analyze whether patients with certain gene mutations experience more side effects than others.
Hint: Place "Gene_Name" and "Mutation_Status" in the Rows field and "Side_Effects" in the Values field, summarizing "Side_Effects" as a count.
How it Helps: Understands the genetic predisposition to side effects.
Business Impact: Helps in refining drug formulations to reduce side effects based on patient genetic profiles.
Survival Rate by Progression-Free Survival
Question: Analyze the relationship between survival rates and progression-free survival.
Hint: Use a Scatter Plot in Excel with "Progression_Free_Survival" on the X-axis and "Survival_Rate" on the Y-axis.
How it Helps: Shows whether a longer progression-free survival translates into higher overall survival rates.
Business Impact: Helps evaluate the long-term benefits of certain treatments based on disease progression.
Drug Success Rate by Trial Phase
Question: Analyze the success rate of drugs based on the phase of the clinical trial they are in.
Hint: Use "Trial_Phase" in the Rows field and "Success_Indicator" in the Values field, summarizing "Success_Indicator" as an average.
How it Helps: Identifies how drug success varies depending on the stage of the clinical trial.
Business Impact: Helps allocate resources effectively by focusing on drugs that perform well in earlier trial phases.

How These Questions Help the Company
Drug Efficacy Insights: By analyzing drug efficacy across demographics, the company can improve its personalized medicine approach, ensuring that patients receive the most effective treatment based on their specific profiles.
Side Effects and Safety Improvements: Identifying patterns in side effects across different drugs and patient profiles will help Pfizer minimize adverse reactions and improve patient safety, leading to better regulatory outcomes.
Optimizing Treatment Plans: Correlating treatment duration, side effects, and efficacy helps design more optimal treatment plans that balance patient well-being with the best possible outcomes.
Targeting Diverse Populations: Understanding how different ethnicities, genders, and age groups respond to treatment ensures inclusivity in clinical trials, increasing the overall success of Pfizer's drug development programs.
Resource Allocation: Analyzing drug success rates by trial phase and patient outcomes helps allocate resources efficiently, prioritizing the drugs with the best potential for future success.


Visualisation Based Questions
1. Age Distribution of Patients
Question: Create a histogram to show the distribution of patient ages.
Hint (Step-by-Step Guide):
Select the "Age" column in your dataset.
Go to the Insert tab on the ribbon.
In the Charts group, click on Insert Statistic Chart.
Choose Histogram from the dropdown.
Adjust the bin ranges to group ages (e.g., 18-30, 31-50, etc.).
How it Helps: Provides an overview of the age range of patients participating in clinical trials.
Business Impact: Helps identify the most common age groups in trials, assisting in better-targeted trial recruitment.

2. Gender Breakdown of Participants
Question: Create a pie chart to visualize the gender distribution of patients.
Hint (Step-by-Step Guide):
Create a summary table for "Gender" by counting the occurrences of each category.
Select the summary data.
Go to the Insert tab.
Click on Insert Pie Chart and select the 2D Pie option.
Customize the chart by adding data labels to show percentages.
How it Helps: Shows gender representation in clinical trials.
Business Impact: Ensures diversity in clinical trials and identifies any gender gaps.

3. Drug Distribution by Trial Phase
Question: Create a stacked bar chart to show the distribution of different drugs across various trial phases.
Hint (Step-by-Step Guide):
Create a Pivot Table with "Drug_Name" in Rows and "Trial_Phase" in Columns.
Drag "Trial_Phase" into the Values area, using Count.
Select the Pivot Table and go to the Insert tab.
Choose Insert Column or Bar Chart and select Stacked Bar.
Customize the chart by adding chart titles and labels.
How it Helps: Illustrates how different drugs are progressing through clinical trials.
Business Impact: Helps in prioritizing drugs that are in later phases of trials.

4. Average Efficacy Score by Drug
Question: Create a bar chart showing the average efficacy score for each drug.
Hint (Step-by-Step Guide):
Create a Pivot Table with "Drug_Name" in Rows and "Efficacy_Score" in Values.
Summarize the "Efficacy_Score" by average.
Select the Pivot Table and go to the Insert tab.
Click on Insert Column or Bar Chart and choose Clustered Bar.
Customize the chart by adding axis titles and adjusting the layout for clarity.
How it Helps: Shows which drugs are performing the best in terms of patient response.
Business Impact: Assists in determining which drugs are most promising for further development.

5. Side Effects by Drug
Question: Create a clustered bar chart to compare the number of side effects reported for each drug.
Hint (Step-by-Step Guide):
Create a Pivot Table with "Drug_Name" in Rows and "Side_Effects" in Values.
Summarize the "Side_Effects" by count.
Select the Pivot Table and go to the Insert tab.
Choose Insert Column or Bar Chart and select Clustered Bar.
Add axis titles and labels to make the chart more informative.
How it Helps: Shows the side effect profile of different drugs.
Business Impact: Helps in identifying drugs with high levels of adverse events, informing safety improvements.

6. Survival Rate by Drug
Question: Create a line chart to visualize the average survival rate for each drug.
Hint (Step-by-Step Guide):
Create a Pivot Table with "Drug_Name" in Rows and "Survival_Rate" in Values.
Summarize the "Survival_Rate" by average.
Select the Pivot Table and go to the Insert tab.
Click on Insert Line or Area Chart and choose Line with Markers.
Customize the chart with axis labels, titles, and data markers.
How it Helps: Shows how effective different drugs are in improving patient survival rates.
Business Impact: Helps focus research on drugs with higher survival rates.

7. Success Rate by Gender
Question: Create a stacked column chart showing the success rate of treatments for different genders.
Hint (Step-by-Step Guide):
Create a Pivot Table with "Gender" in Rows and "Success_Indicator" in Values.
Summarize the "Success_Indicator" by average.
Select the Pivot Table and go to the Insert tab.
Choose Insert Column or Bar Chart and select Stacked Column.
Format the chart to display the success rate clearly by gender.
How it Helps: Shows which gender is experiencing more treatment success.
Business Impact: Helps improve treatment plans tailored by gender.

8. Side Effects vs. Treatment Outcome
Question: Create a scatter plot to show the relationship between side effects and treatment outcomes.
Hint (Step-by-Step Guide):
Select the columns for "Side_Effects" and "Treatment_Outcome".
Go to the Insert tab.
Click on Insert Scatter (X, Y) or Bubble Chart and choose Scatter.
Format the chart by adding axis titles and markers.
How it Helps: Shows the correlation between the number of side effects and treatment outcomes.
Business Impact: Helps identify whether more side effects are linked to poorer treatment outcomes.

9. Biomarker Level by Drug
Question: Create a box plot to compare the distribution of biomarker levels across different drugs.
Hint (Step-by-Step Guide):
Select the columns for "Drug_Name" and "Biomarker_Level".
Go to the Insert tab.
Click on Insert Statistic Chart and choose Box and Whisker.
Format the chart to clearly show the biomarker level distribution.
How it Helps: Shows the variability in biomarker levels across different drugs.
Business Impact: Helps understand how drugs affect biomarker levels, which can guide precision treatments.

10. Progression-Free Survival by Drug
Question: Create a line chart to show the progression-free survival for each drug.
Hint (Step-by-Step Guide):
Create a Pivot Table with "Drug_Name" in Rows and "Progression_Free_Survival" in Values.
Summarize "Progression_Free_Survival" by average.
Select the Pivot Table and go to the Insert tab.
Click on Insert Line Chart and select Line.
Customize the chart with markers and axis titles for clarity.
How it Helps: Shows which drugs help patients live longer without disease progression.
Business Impact: Guides further research into drugs with higher progression-free survival rates.



11. Success Rate by Age Group
Question: Create a column chart showing the success rate of treatments for different age groups.
Hint (Step-by-Step Guide):
Create a Pivot Table with "Age" in Rows and "Success_Indicator" in Values.
Group "Age" into ranges (e.g., 18-30, 31-50).
Summarize the "Success_Indicator" by average.
Select the Pivot Table and go to the Insert tab.
Choose Insert Column or Bar Chart and select Clustered Column.
How it Helps: Shows how treatment success varies across age groups.
Business Impact: Helps in designing age-specific treatment plans for better success rates.

12. Efficacy Score Distribution by Gene Mutation
Question: Create a box plot to compare the efficacy score distribution across different gene mutations.
Hint (Step-by-Step Guide):
Select the columns for "Gene_Name" and "Efficacy_Score".
Go to the Insert tab.
Click on Insert Statistic Chart and select Box and Whisker.
Customize the chart by adding axis titles and formatting the box plots.
How it Helps: Shows how gene mutations impact drug efficacy.
Business Impact: Helps in tailoring treatments based on patient genetics.

13. Adverse Events by Age Group
Question: Create a clustered column chart to compare the number of adverse events reported across different age groups.
Hint (Step-by-Step Guide):
Create a Pivot Table with "Age" in Rows and "Adverse_Events" in Values.
Group the "Age" column into ranges (e.g., 18-30, 31-50).
Summarize the "Adverse_Events" by count.
Select the Pivot Table and go to the Insert tab.
Choose Insert Column or Bar Chart and select Clustered Column.
How it Helps: Highlights which age groups are most affected by adverse events.
Business Impact: Helps design age-specific drug safety measures to reduce side effects.


14. Progression-Free Survival by Mutation Status
Question: Create a bar chart comparing the average progression-free survival based on mutation status.
Hint (Step-by-Step Guide):
Create a Pivot Table with "Mutation_Status" in Rows and "Progression_Free_Survival" in Values.
Summarize the "Progression_Free_Survival" by average.
Select the Pivot Table and go to the Insert tab.
Click on Insert Column or Bar Chart and select Clustered Bar.
Customize the chart with labels and titles.
How it Helps: Shows whether patients with specific mutations have better or worse progression-free survival.
Business Impact: Helps in tailoring treatments to genetic mutations for better progression outcomes.

15. Success Rate by Trial Phase
Question: Create a line chart to compare the success rate of treatments across different clinical trial phases.
Hint (Step-by-Step Guide):
Create a Pivot Table with "Trial_Phase" in Rows and "Success_Indicator" in Values.
Summarize the "Success_Indicator" by average.
Select the Pivot Table and go to the Insert tab.
Click on Insert Line Chart and select Line with Markers.
Customize the chart with titles, labels, and data markers for clarity.
How it Helps: Illustrates how success rates vary across different trial phases.
Business Impact: Helps the company understand which trial phases show higher success, aiding in resource allocation.



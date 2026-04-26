Dream Fertility Clinic Health Insights: Uncovering Risk Factors & Diagnoses for 2022
<img width="1868" height="847" alt="Dashboard" src="https://github.com/user-attachments/assets/1092c4b9-7dcd-4755-bdfb-1f15e80173b9" />

1.	Outline:
•	Introduction 
•	Story of Data
•	Data Splitting and Pre-processing 
•	Pre-Analysis 
•	In-Analysis
•	Post-Analysis and Insights 
•	Data Visualisations & Charts 
•	Recommendations and Observations 
•	Conclusion 
•	References

3.	Introduction: 
In the realm of reproductive health, understanding the interplay between lifestyle factors, medical history, and fertility outcomes is crucial for developing effective interventions. The Dream Fertility Clinic dataset for 2022 provides a comprehensive view of patient profiles, capturing key variables such as age, sedentary behavior (hours spent sitting per day), frequency of alcohol consumption, smoking habits, seasonal influences, childhood diseases, accidents or serious trauma, surgical interventions, and high fever occurrences in the last year, culminating in binary diagnosis outcomes ("Normal" or "Altered"). This analysis seeks to uncover how these risk factors correlate with fertility diagnoses, revealing patterns that could inform preventive strategies, personalised treatments, and resource allocation to optimise patient outcomes and reduce healthcare costs.

2.1	Objective of the Project:

1.	To identify risk factors, like smoking, alcohol, and sedentary behaviour most strongly correlate with specific diagnoses to inform health strategies.
   
3.	To explore trends and patterns by analysing how age, season, or past events influence health.
   
4.	To provide stakeholders with visualisations and summaries to optimise treatment, reduce costs, and enhance patient outcomes.
   
5.	Explore correlations between lunch type and academic outcomes.
   
6.	Provide actionable insights to educators and policymakers to improve student support.

   
2.2	Methodology:


The analysis was conducted using Microsoft Excel, leveraging pivot tables, charts, and descriptive statistics for exploratory data analysis. The dataset was pre-cleaned to ensure accuracy, with all visualisations and dashboards adhering to principles of consistency (uniform colour schemes, labelling) and clarity (intuitive axes, legends). Key visualisations included stacked bar charts for surgical interventions by diagnosis, column charts for alcohol frequency versus sedentary hours, bar charts for age-based sitting averages, clustered columns for trauma/diagnosis/fever interactions, line graphs for age-alcohol trends, doughnut charts for smoking/diagnosis and seasonal fevers, and scatter plots for sitting duration distributions. These tools effectively highlighted trends, such as seasonal fever peaks and age-sedentary correlations.
 
Story of the Data: 


It captures health-related factors and lifestyle habits of individuals, culminating in a "Diagnosis" outcome that is a medical condition or classification. Consider a group of people from diverse backgrounds, monitored across seasons, whose early life experiences, like childhood diseases or trauma, and current behaviours, such as alcohol use, smoking, and sedentary time, are recorded in concert with acute events like fevers and surgeries. The story that would emerge is one of patterns, perhaps younger individuals with high sedentary hours and frequent alcohol consumption are more susceptible to certain types of diagnoses, while those who have experienced trauma prove resilient or susceptible. Given time, this would surface how environmental factors, such as seasons, interact with personal habits to determine health outcomes and provide the ability for preventive care. For example, this data could unveil a "cautionary tale" in which disregard for lifestyle risks resulted in negative diagnoses, or an "inspiring one" in which early interventions improve risks, turning raw data into actionable insights relevant for healthcare providers and individuals.

3.	Data Splitting and Preprocessing
   
a. Data Cleaning Process:

Preparation Steps

Loaded the dataset (CSV from Kaggle) into a new Excel workbook. Applied filters, conditional formatting, and sorting to flag issues like blank cells, outliers (e.g., sedentary hours exceeding 24, invalid categorical entries like non-standard alcohol frequency labels), and inconsistencies (e.g., mixed cases in "Season" or "Smoking Habit").
Duplicated the original sheet as “Raw Data” to preserve an unaltered backup for auditability and reproducibility.

Core Cleaning Techniques
Remove Duplicates: Utilised Data > Remove Duplicates based on unique identifiers (e.g., implicit patient IDs or composite keys from age/season/diagnosis), eliminating ~1–3% redundant records while retaining unique profiles.

Handle Missing Values: Identified blanks in critical fields (e.g., "Number of Hours Spent Sitting," "Diagnosis," "High Fever") via Find & Select > Go To Special. Removed rows with >50% missing data (e.g., incomplete lifestyle profiles); imputed categoricals with mode (e.g., "Frequency of Alcohol Consumption") and numerics with median (e.g., sitting hours by age group) to minimise bias.

Standardise Text and Categories: Employed Find & Replace, TRIM, and Text to Columns for uniformity. e.g., standardising "Diagnosis" to "Normal"/"Altered," "Smoking Habit" to consistent yes/no or frequency scales, "Season" to "Spring/Summer/Fall/Winter," and binary flags like "Accident or Serious Trauma" to "Yes/No."

Data Type Corrections: Converted text-formatted numerics (e.g., "Age," "Number of Hours Spent Sitting") to proper numeric types using Text to Columns and Number Format; ensured dates/seasons were categorical.

Finalisation

Validated via pivot table summaries (e.g., counts by diagnosis, averages for sitting hours) and descriptive stats (e.g., =AVERAGE (), =COUNTIF ()). Documented all changes in a changelog sheet, confirming data integrity for downstream analyses like age-sedentary averages (e.g., 20.2 hours at age 30) and fever counts (e.g., 37 in spring). This process reduced noise, enabling reliable insights into risk factors like compounded alcohol-sedentary effects on "Altered" diagnoses. 

Potential Challenges:


•	Missing values in subjective fields like "Frequency of Alcohol Consumption" or "Smoking Habit" could skew results.

•	Variables like "Childish Diseases" or "Accident or Serious trauma" are binary (yes/no) but lack standardisation, complicating aggregation. 

•	Lifestyle factors might correlate with diagnoses but not cause them.


5.	Data Splitting:
   
KEY METRICS:


Metrics - Numerical:

-	Age.
  
-	Number of Hours Spent Sitting per Day.
  
KEY DIMENSIONS:


-	Frequency Of Alcohol Consumption.
-	
-	Season.
-	
-	Childish Diseases.
-	
-	Accident or Serious trauma.
-	
-	Surgical Intervention.
-	
-	Smoking Habit.
-	
-	Diagnosis.
-	
-	High Fever in the last Year.

  
5.	Potential Analysis Questions:
•	How does age distribution vary across frequent alcohol usage?

•	Are certain conditions more common in specific age groups?

•	What is the relationship between "Frequency of Alcohol Consumption" and "Number of Hours Spent Sitting" with diagnosis outcomes?

•	Does higher sedentary time ("Number of Hours Spent Sitting per Day") increase the risk for certain diagnoses?

•	Does age affect the average number of hours spent sitting per day?

•	How might past events such as "Childhood Diseases," "Accident or Serious Trauma," or "Surgical Intervention" impact current diagnoses?

•	Are there any seasonal patterns, such as higher fevers in winter leading to certain outcomes?

7.	Pre-Analysis Insights:
8.	
•	Older age groups could show higher sedentary averages, correlating with increased risk for diagnoses like cardiovascular issues. In comparison, younger groups might have lower averages linked to fewer such conditions, highlighting age as a moderator for sedentary-related health risks.

•	Heavy smokers might overlap with frequent alcohol users, showing age variations (e.g., younger heavy users) and compounded risks for diagnoses, such as when paired with high sedentary time, potentially increasing outcomes like addiction-related or chronic conditions.

•	Individuals with childhood diseases might show higher diagnosis rates in adulthood (e.g., immune vulnerabilities), especially if combined with sedentary time or alcohol use, illustrating long-term impacts on outcomes like chronic illnesses.

•	Trauma survivors might report higher fevers, potentially worsening diagnoses (e.g., stress-related issues), with winter exacerbations linking past events to seasonal health declines.

•	Higher surgery counts could correlate with severe diagnoses (e.g., post-trauma recoveries), revealing how interventions influence outcomes, especially when sedentary time or alcohol use is high, potentially increasing risks for complications.

•	Frequent alcohol users might skew younger, with higher sedentary time compounding risks for diagnoses like liver issues, showing age as a factor in lifestyle-diagnosis links.


10.	In-Analysis Observations:
11.	
ANALYSIS: Frequency of Surgical Intervention By Diagnosis

•	Individuals who underwent surgical interventions (categorised as "Yes") accounted for 50 diagnoses in total, with 43 cases falling under the "Normal" diagnosis and 7 under the "Altered" diagnosis.

•	Individuals without surgical interventions (categorised as "No") accounted for 49 diagnoses in total, with 44 cases under the "Normal" diagnosis and 5 under the "Altered" diagnosis.

ANALYSIS: Frequency of Alcohol Consumption By Number of Hours Sitting Per Day

•	Individuals who consume alcohol once a week accumulate a total of 640 hours spent sitting per day.

•	Individuals who rarely or never consume alcohol accumulate a total of 303 hours spent sitting per day.

•	Individuals who consume alcohol several times a week accumulate a total of 116 hours spent sitting per day.

•	Individuals who consume alcohol daily accumulate a total of 11 hours spent sitting per day.

•	Individuals who consume alcohol several times a day accumulate a total of 5 hours spent sitting per day.

ANALYSIS: Age by Average Number of Hours Spent Sitting Per Day

•	Individuals aged 30 spend the most time sitting daily, with an average of about 20.2 hours.

•	Individuals aged 27 have an average of approximately 10.3 hours spent sitting per day.

•	Individuals aged 28 have an average of approximately 9.0 hours spent sitting per day.

•	Individuals aged 29 have an average of 8.6 hours spent sitting per day.

•	Individuals aged 33 have an average of approximately 6.3 hours spent sitting per day.

•	Individuals aged 35 have an average of approximately 6.3 hours spent sitting per day.

•	Individuals aged 34 have an average of approximately 6.0 hours spent sitting per day.

•	Individuals aged 36 have an average of approximately 6.0 hours spent sitting per day.

•	Individuals aged 32 have an average of approximately 5.2 hours spent sitting per day.

•	Individuals aged 31 have an average of approximately 3.0 hours spent sitting per day.

ANALYSIS: Accident or Serious Trauma and Diagnosis By High Fever

•	Individuals without a history of accident or serious trauma show diagnoses in both "Normal" and "Altered" categories, with the "Normal" diagnosis linked to the highest fever count of 46 and the "Altered" diagnosis to 9 fever counts.

•	Individuals with a history of accident or serious trauma (categorised as "Yes") also show diagnoses in both "Normal" and "Altered" categories, with the "Normal" diagnosis linked to 41 fever counts and the "Altered" diagnosis to 3 fever counts.

ANALYSIS: Age by Count of Frequency of Alcohol Consumption

•	Age 27 represents 7.07% of the total counts for alcohol consumption frequency.

•	Age 28 has the highest percentage, at 28.28%, for alcohol consumption frequency.

•	Age 29 represents 5.05% of the total counts for alcohol consumption frequency.

•	Age 30 represents 26.26% of the total counts for alcohol consumption frequency.

•	Age 31 represents 2.02% of the total counts for alcohol consumption frequency.

•	Age 32 represents 17.17% of the total counts for alcohol consumption frequency.

•	Age 33 represents 7.07% of the total counts for alcohol consumption frequency.

•	Age 34 represents 1.01% of the total counts for alcohol consumption frequency.

•	Age 35 represents 4.04% of the total counts for alcohol consumption frequency.

•	Age 36 represents 2.02% of the total counts for alcohol consumption frequency.

ANALYSIS: Diagnosis By Counts of Smoking Habit

•	Individuals with a "Normal" diagnosis show the highest smoking habit count, totalling 87.

•	Individuals with an "Altered" diagnosis show the lowest smoking habit count, totalling 12.

ANALYSIS: Season by Counts of High Fever

•	The spring season records the highest number of high fever cases, with 37 instances.

•	The fall season records 30 instances of high fever.

•	The winter season records 28 instances of high fever.

•	The summer season has the fewest high fever cases, with only 4 instances, marking a significant decrease from spring's peak.

ANALYSIS: Number of Hours Spent Sitting By Counts of Number of Hours Spent Sitting Per Day

•	Individuals sitting for 9 hours daily account for 16 cases of that sitting duration.

•	Individuals sitting for 5 hours daily account for 16 cases of that sitting duration.

•	Individuals sitting for 7 hours daily account for 13 cases of that sitting duration.

•	Individuals sitting for 6 hours daily account for 11 cases of that sitting duration.

•	Individuals sitting for 3 hours daily account for 10 cases of that sitting duration.

•	Individuals sitting for 11 hours daily account for 10 cases of that sitting duration.

•	Individuals sitting for 8 hours daily account for 10 cases of that sitting duration.

•	Individuals sitting for 16 hours daily account for 3 cases of that sitting duration.

•	Individuals sitting for 14 hours daily account for 3 cases of that sitting duration.

•	Individuals sitting for 1-hour daily account for 2 cases of that sitting duration.

•	Individuals sitting for 10 hours daily account for 2 cases of that sitting duration.

•	Individuals sitting for 2 hours daily account for 1 case of that sitting duration.

•	Individuals sitting 18 hours daily account for 1 case of that sitting duration. 342 hours.


12.	In-Analysis Recommendations:
13.	
ANALYSIS: Frequency of Surgical Intervention By Diagnosis

•	Encourage routine post-surgical follow-ups for individuals with interventions to monitor for potential shifts toward "Altered" diagnoses, potentially reducing the 7 cases observed.

•	Promote preventive health screenings for those without surgical history to maintain the higher "Normal" diagnosis rates, as seen in the 44 cases.

•	Integrate surgical data into predictive models to identify at-risk patients early, aiming to balance the slight edge in "Normal" outcomes for non-intervention groups.


ANALYSIS: Frequency of Alcohol Consumption By Number of Hours Sitting Per Day

•	Advise moderate alcohol consumers, such as once a week) to incorporate more physical activity to offset the high sedentary hours of 640, potentially lowering associated health risks.

•	Support non-drinkers in maintaining low sedentary time (303 hours) through wellness programs, as this group shows balanced habits.

•	Implement targeted interventions for frequent drinkers (daily or several times a day) to reduce both consumption and sitting time, addressing the lower but still notable hours observed.

ANALYSIS: Age by Average Number of Hours Spent Sitting Per Day


•	Target age 30 individuals with sedentary reduction programs, given their high average of 20.2 hours, to mitigate long-term health impacts.

•	Encourage younger adults, such as ages 27-29) to sustain or improve their lower sitting averages through active lifestyles, building on the 10.3-to-8.6-hour ranges.

•	Promote workplace ergonomics and breaks for mid-30s groups, such as ages 33-36) to further decrease their 6.0-6.3-hour averages, fostering healthier aging.

•	Individuals aged 36 have an average of approximately 6.0 hours spent sitting per day.

•	Individuals aged 32 have an average of approximately 5.2 hours spent sitting per day.

•	Individuals aged 31 have an average of approximately 3.0 hours spent sitting per day.

ANALYSIS: Accident or Serious Trauma and Diagnosis By High Fever


•	Provide trauma-informed care for affected individuals to address the fever disparities, aiming to elevate "Normal" diagnosis rates from 41 to closer to 46.

•	Develop fever monitoring protocols for all patients, especially those with trauma history, to prevent escalation in "Altered" cases (3 observed).

•	Offer counseling and support services post-trauma to reduce fever-related risks, potentially improving overall diagnosis outcomes.

ANALYSIS: Age by Count of Frequency of Alcohol Consumption


•	Focus alcohol education campaigns on peak age groups like 28 (28.28%) and 30 (26.26%) to promote moderation and reduce consumption frequencies.

•	Tailor interventions for younger adults, like ages 27-29 to address emerging habits, leveraging their 5.05%-7.07% shares.

•	Encourage healthy aging strategies for older groups, like ages 32-36) to maintain lower frequencies, building on their 1.01%-17.17% distributions.

ANALYSIS: Diagnosis by Counts of Smoking Habit


•	Implement smoking cessation programs for "Normal" diagnosis groups to further lower the 87 count and prevent potential shifts to "Altered" states.

•	Monitor and support "Altered" diagnosis individuals with low smoking (12 count) through integrated health plans to sustain positive outcomes.

•	Use these counts to inform public health policies, emphasizing smoking's role in diagnosis variations for broader community impact.

ANALYSIS: Season by Counts of High Fever


•	Enhance fever prevention measures during spring (37 cases) through vaccinations or hygiene campaigns to curb seasonal spikes.

•	Prepare seasonal health resources for fall and winter (30 and 28 cases) to manage fever risks effectively.

•	Promote outdoor activities in summer to maintain low fever rates (4 cases), encouraging year-round wellness habits.

ANALYSIS: Number of Hours Spent Sitting By Counts of Number of Hours Spent Sitting Per Day


•	Advise individuals with high sitting durations, like 9-11 hours, 10-16 cases) to adopt standing desks or breaks to reduce health risks.

•	Promote balanced routines for moderate sitters, like 5-8 hours, 11-16 cases) to prevent escalation toward extremes.

•	Encourage active lifestyles for low sitters, like 1-3 hours, 1-10 cases) and provide resources for those at very high levels (14-18 hours, 1-3 cases) to improve overall well-being.

15. Data Visualisations:

16. 
•	Frequency of Surgical Intervention by Diagnosis: A stacked bar chart was used.

 
•	Frequency of Alcohol Consumption By Number of Hours Sitting /Day: Column chart was used.
 
•	Age By Average Number of Hours Spent Sitting: A bar chart was used
 
•	Accident or Serious Trauma & Diagnosis by High Fever: A clustered column chart was used.
 
•	Age By Count of Frequency of Alcohol Consumption: A line graph was used
 
•	Diagnosis by Counts of Smoking Habit: A doughnut chart was used
 
•	Season by Counts of High Fever: A doughnut chart was used
 
•	No of Hours Spent Sitting By Count of No of Hours Spent Sitting Per Day: Scatter Plot was used
 
11. Observations and Recommendations:
    
11.1. Post-Analysis Observations:

ANALYSIS: Diagnosis (Normal)


•	Diagnosis under the "Normal" category has age by count of frequency of alcohol consumption, generating results where Age 27 represents 6.90% of the total counts for alcohol consumption frequency. Age 28 has the highest percentage, at 32.18%, for alcohol consumption frequency. Age 29 represents 5.75% of the total counts for alcohol consumption frequency. Age 30 represents 21.84% of the total counts for alcohol consumption frequency. Age 31 represents 2.30% of the total counts for alcohol consumption frequency. Age 32 represents 16.09% of the total counts for alcohol consumption frequency. Age 33 represents 8.05% of the total counts for alcohol consumption frequency. Age 34 represents 1.15% of the total counts for alcohol consumption frequency. Age 35 represents 3.45% of the total counts for alcohol consumption frequency. Age 36 represents 2.30% of the total counts for alcohol consumption frequency. Individuals sitting for 9 hours daily account for 16 cases of that sitting duration. Individuals sitting for 5 hours daily account for 16 cases of that sitting duration. Individuals sitting for 7 hours daily account for 13 cases of that sitting duration. Individuals sitting for 6 hours daily account for 11 cases of that sitting duration. Individuals sitting for 3 hours daily account for 10 cases of that sitting duration. Individuals sitting for 11 hours daily account for 10 cases of that sitting duration. Individuals sitting for 8 hours daily account for 10 cases of that sitting duration. Individuals sitting for 16 hours daily account for 3 cases of that sitting duration. Individuals sitting for 14 hours daily account for 3 cases of that sitting duration. Individuals sitting for 1 hour daily account for 2 cases of that sitting duration. Individuals sitting for 10 hours daily account for 2 cases of that sitting duration. Individuals sitting for 2 hours daily account for 1 case of that sitting duration. Individuals sitting 18 hours daily account for 1 case of that sitting duration. 342 hours. For the frequency of surgical Intervention by diagnosis under the "Normal" category, Individuals who underwent surgical interventions (categorised as "Yes") accounted for 43 diagnoses, while individuals without surgical interventions (categorised as "No") accounted for 44 diagnoses. The spring season records the highest number of high fever cases, with 33 instances. The fall season records 24 instances of high fever. The winter season records 27 instances of high fever. The summer season has the fewest high fever cases, with only 3 instances, marking a significant decrease from spring's peak. Individuals without a history of accident or serious trauma (categorised as "No" show diagnoses in the "Normal" category, with the "Normal" diagnosis linked to the highest fever count of 46. Individuals with a history of accident or serious trauma (categorised as "Yes") also show diagnoses in the "Normal" category, with the "Normal" diagnosis linked to 41 fever counts.


ANALYSIS: Diagnosis (Altered)


•	Diagnosis under the "Altered" category has age by count of frequency of alcohol consumption, generating results where Age 27 represents 8.33% of the total counts for alcohol consumption frequency. Age 30 represents 58.33% of the total counts for alcohol consumption frequency. Age 32 represents 25.00% of the total counts for alcohol consumption frequency. Age 35 represents 8.33% of the total counts for alcohol consumption frequency. Individuals sitting for 9 hours daily account for 16 cases of that sitting duration. Individuals sitting for 5 hours daily account for 16 cases of that sitting duration. Individuals sitting for 7 hours daily account for 13 cases of that sitting duration. Individuals sitting for 6 hours daily account for 11 cases of that sitting duration. Individuals sitting for 3 hours daily account for 10 cases of that sitting duration. Individuals sitting for 11 hours daily account for 10 cases of that sitting duration. Individuals sitting for 8 hours daily account for 10 cases of that sitting duration. Individuals sitting for 16 hours daily account for 3 cases of that sitting duration. Individuals sitting for 14 hours daily account for 3 cases of that sitting duration. Individuals sitting for 1 hour daily account for 2 cases of that sitting duration. Individuals sitting for 10 hours daily account for 2 cases of that sitting duration. Individuals sitting for 2 hours daily account for 1 case of that sitting duration. Individuals sitting 18 hours daily account for 1 case of that sitting duration. 342 hours. For the frequency of surgical Intervention by diagnosis under the "Altered" category, Individuals who underwent surgical interventions (categorised as "Yes") accounted for 7 diagnoses, while individuals without surgical interventions (categorised as "No") accounted for 5 diagnoses. The fall season records the highest number of high fever cases, with 6 instances. The spring season records 4 instances of high fever. The winter season records 1 instance of high fever. The summer season has 1 instance of high fever. Individuals without a history of accident or serious trauma (categorised as "No" show diagnoses in the "Altered" category, with the "Altered" diagnosis linked to the highest fever count of 9. Individuals with a history of accident or serious trauma (categorised as "Yes") also show diagnoses in the "Altered" category, with the "Altered" diagnosis linked to 3 fever counts.


ANALYSIS: Surgical Intervention (No)


•	For analysis on surgical intervention in the "No" category, Age 27 represents 12.24% of the total counts for alcohol consumption frequency. Age 28 has the highest percentage, at 36.73%, for alcohol consumption frequency. Age 29 represents 4.08% of the total counts for alcohol consumption frequency. Age 30 represents 22.45% of the total counts for alcohol consumption frequency. Age 31 represents 2.04% of the total counts for alcohol consumption frequency. Age 32 represents 12.24% of the total counts for alcohol consumption frequency. Age 33 represents 4.08% of the total counts for alcohol consumption frequency. Age 34 represents 2.04% of the total counts for alcohol consumption frequency. Age 35 represents 4.08% of the total counts for alcohol consumption frequency. Individuals sitting for 9 hours daily account for 16 cases of that sitting duration. Individuals sitting for 5 hours daily account for 16 cases of that sitting duration. Individuals sitting for 7 hours daily account for 13 cases of that sitting duration. Individuals sitting for 6 hours daily account for 11 cases of that sitting duration. Individuals sitting for 3 hours daily account for 10 cases of that sitting duration. Individuals sitting for 11 hours daily account for 10 cases of that sitting duration. Individuals sitting for 8 hours daily account for 10 cases of that sitting duration. Individuals sitting for 16 hours daily account for 3 cases of that sitting duration. Individuals sitting for 14 hours daily account for 3 cases of that sitting duration. Individuals sitting for 1 hour daily account for 2 cases of that sitting duration. Individuals sitting for 10 hours daily account for 2 cases of that sitting duration. Individuals sitting for 2 hours daily account for 1 case of that sitting duration. Individuals sitting 18 hours daily account for 1 case of that sitting duration. 342 hours.  For the frequency of surgical Intervention by diagnosis, diagnoses that are under the "Altered" category had individuals who underwent surgical interventions (categorised as "Yes"), accounting for 7 diagnoses, while individuals with frequency of surgical intervention under the "Normal" category had individuals who underwent surgical intervention (categorised as "Yes" accounting for 5 diagnoses. The spring season records the highest number of high fever cases, with 17 instances. The fall season records 15 instances of high fever. The winter season records 14 instances of high fever. The summer season has the fewest high fever cases, with only 3 instances, marking a significant decrease from spring's peak. Individuals without a history of accident or serious trauma show diagnoses in both "Normal" and "Altered" categories, with the "Normal" diagnosis linked to the highest fever count of 28 and the "Altered" diagnosis to 2 fever counts. Individuals with a history of accident or serious trauma (categorised as "Yes") also show diagnoses in both "Normal" and "Altered" categories, with the "Normal" diagnosis linked to 16 fever counts and the "Altered" diagnosis to 3 fever counts.


ANALYSIS: Surgical Intervention (Yes)


•	For analysis on surgical intervention in the "Yes" category, Age 27 represents 2.00% of the total counts for alcohol consumption frequency. Age 28 represents 20.00% of the total counts for alcohol consumption frequency. Age 29 represents 6.00% of the total counts for alcohol consumption frequency.  Age 30 has the highest percentage, at 30.00%, for alcohol consumption frequency.  Age 31 represents 2.00% of the total counts for alcohol consumption frequency. Age 32 represents 22.00% of the total counts for alcohol consumption frequency. Age 33 represents 10.00% of the total counts for alcohol consumption frequency. Age 35 represents 4.00% of the total counts for alcohol consumption frequency. Age 35 represents 4.00% of the total counts for alcohol consumption frequency. Individuals sitting for 9 hours daily account for 16 cases of that sitting duration. Individuals sitting for 5 hours daily account for 16 cases of that sitting duration. Individuals sitting for 7 hours daily account for 13 cases of that sitting duration. Individuals sitting for 6 hours daily account for 11 cases of that sitting duration. Individuals sitting for 3 hours daily account for 10 cases of that sitting duration. Individuals sitting for 11 hours daily account for 10 cases of that sitting duration. Individuals sitting for 8 hours daily account for 10 cases of that sitting duration. Individuals sitting for 16 hours daily account for 3 cases of that sitting duration. Individuals sitting for 14 hours daily account for 3 cases of that sitting duration. Individuals sitting for 1 hour daily account for 2 cases of that sitting duration. Individuals sitting for 10 hours daily account for 2 cases of that sitting duration. Individuals sitting for 2 hours daily account for 1 case of that sitting duration. Individuals sitting for 18 hours daily account for 1 case of that sitting duration. 342 hours.  For the frequency of surgical Intervention by diagnosis, diagnoses that are under the "Altered" category had individuals who underwent surgical interventions (categorised as "Yes"), accounting for 7 diagnoses, while individuals with frequency of surgical intervention under the "Normal" category had individuals who underwent surgical intervention (categorised as "Yes" accounting for 43 diagnoses. The spring season records the highest number of high fever cases, with 20 instances. The fall season records 15 instances of high fever. The winter season records 14 instances of high fever. The summer season has the fewest high fever cases, with only 1 instance, marking a significant decrease from spring's peak. Individuals without a history of accident or serious trauma show diagnoses in both "Normal" and "Altered" categories, with the "Normal" diagnosis linked to the highest fever count of 18 and the "Altered" diagnosis to 7 fever counts. Individuals with a history of accident or serious trauma (categorised as "Yes") show diagnoses in "Normal" categories, with the "Normal" diagnosis linked to 25 fever counts.

ANALYSIS: Season (Fall)


•	The fall season has individuals with 30 cases of high fever. Analysis shows age by count of frequency of alcohol consumption, generating results where Age 28 represents 30.00% of the total counts for alcohol consumption frequency. Age 29 represents 6.67% of the total counts for alcohol consumption frequency. Age 30 represents 36.67% of the total counts for alcohol consumption frequency. Age 32 represents 16.67% of the total counts for alcohol consumption frequency. Age 33 represents 6.67% of the total counts for alcohol consumption frequency. Age 35 represents 3.33% of the total counts for alcohol consumption frequency. Individuals sitting for 9 hours daily account for 16 cases of that sitting duration. Individuals sitting for 5 hours daily account for 16 cases of that sitting duration. Individuals sitting for 7 hours daily account for 13 cases of that sitting duration. Individuals sitting for 6 hours daily account for 11 cases of that sitting duration. Individuals sitting for 3 hours daily account for 10 cases of that sitting duration. Individuals sitting for 11 hours daily account for 10 cases of that sitting duration. Individuals sitting for 8 hours daily account for 10 cases of that sitting duration. Individuals sitting for 16 hours daily account for 3 cases of that sitting duration. Individuals sitting for 14 hours daily account for 3 cases of that sitting duration. Individuals sitting for 1 hour daily account for 2 cases of that sitting duration. Individuals sitting for 10 hours daily account for 2 cases of that sitting duration. Individuals sitting for 2 hours daily account for 1 case of that sitting duration. Individuals sitting for 18 hours daily account for 1 case of that sitting duration. 342 hours. For the frequency of surgical Intervention by diagnosis, diagnoses that are under the "Altered" category had individuals who underwent surgical interventions (categorised as "Yes"), accounting for 4 diagnoses, while individuals with frequency of surgical intervention under the "Normal" category had individuals who underwent surgical intervention (categorised as "Yes"), accounting for 11 diagnoses. Individuals without a history of accident or serious trauma (categorised as "No" show diagnoses in the "Altered" category, with the "Altered" diagnosis linked to the fever count of 2. Individuals with a history of accident or serious trauma (categorised as "No") also show diagnoses in the "Normal" category, with the "Normal" diagnosis linked to 13 fever counts. Individuals without a history of accident or serious trauma show diagnoses in both "Normal" and "Altered" categories, with the "Normal" diagnosis linked to the highest fever count of 15 and the "Altered" diagnosis to 5 fever counts. Individuals with a history of accident or serious trauma (categorised as "Yes") also show diagnoses in both "Normal" and "Altered" categories, with the "Normal" diagnosis linked to 9 fever counts and the "Altered" diagnosis to 1 fever count.

ANALYSIS: Season (Spring)


•	The Spring season has individuals with 37 cases of high fever. Analysis shows age by count of frequency of alcohol consumption, generating results where Age 27 represents 16.22% of the total counts for alcohol consumption frequency. Age 28 represents 21.62% of the total counts for alcohol consumption frequency. Age 29 represents 2.70% of the total counts for alcohol consumption frequency. Age 30 represents 18.92% of the total counts for alcohol consumption frequency. Age 31 represents 2.70% of the total counts for alcohol consumption frequency. Age 32 represents 13.51% of the total counts for alcohol consumption frequency. Age 33 represents 10.81% of the total counts for alcohol consumption frequency. Age 34 represents 2.70% of the total counts for alcohol consumption frequency. Age 35 represents 8.11% of the total counts for alcohol consumption frequency. Age 36 represents 2.70% of the total counts for alcohol consumption frequency. Individuals sitting for 9 hours daily account for 16 cases of that sitting duration. Individuals sitting for 5 hours daily account for 16 cases of that sitting duration. Individuals sitting for 7 hours daily account for 13 cases of that sitting duration. Individuals sitting for 6 hours daily account for 11 cases of that sitting duration. Individuals sitting for 3 hours daily account for 10 cases of that sitting duration. Individuals sitting for 11 hours daily account for 10 cases of that sitting duration. Individuals sitting for 8 hours daily account for 10 cases of that sitting duration. Individuals sitting for 16 hours daily account for 3 cases of that sitting duration. Individuals sitting for 14 hours daily account for 3 cases of that sitting duration. Individuals sitting for 1-hour daily account for 2 cases of that sitting duration. Individuals sitting for 10 hours daily account for 2 cases of that sitting duration. Individuals sitting for 2 hours daily account for 1 case of that sitting duration. Individuals sitting for 18 hours daily account for 1 case of that sitting duration. 342 hours. For the frequency of surgical Intervention by diagnosis, diagnoses that are under the "Altered" category had individuals who underwent surgical interventions (categorised as "Yes"), accounting for 19 diagnoses, while individuals with frequency of surgical intervention under the "Normal" category had individuals who underwent surgical intervention (categorised as "No"), accounting for 14 diagnoses. Individuals without a history of accident or serious trauma (categorised as "No" show diagnoses in the "Altered" category, with the "Altered" diagnosis linked to the fever count of 3. Individuals with a history of accident or serious trauma (categorised as "No") also show diagnoses in the "Normal" category, with the "Normal" diagnosis linked to 13 fever counts. Individuals without a history of accident or serious trauma show diagnoses in both "Normal" and "Altered" categories, with the "Normal" diagnosis linked to the fever count of 12 and the "Altered" diagnosis to 2 fever counts. Individuals with a history of accident or serious trauma (categorised as "Yes") also show diagnoses in both "Normal" and "Altered" categories, with the "Normal" diagnosis linked to 21 fever counts and the "Altered" diagnosis to 2 fever counts.


11.2 Post-Analysis Recommendations:

ANALYSIS: Diagnosis (Normal)

High Priority: 

•	Implement immediate alcohol moderation programs for high-frequency groups like Age 28 (32.18%) to reduce risks associated with "Normal" diagnoses, given the elevated consumption patterns. 

•	Provide urgent counselling for those with prolonged sitting (e.g., 9 hours, 16 cases) to prevent health deterioration in "Normal" cases.

Medium Priority: 

•	Promote ergonomic adjustments for those with prolonged sitting (e.g., 9-11 hours, 10-16 cases) to prevent escalation toward health issues in "Normal" cases. 

•	Develop targeted fever monitoring for spring (33 cases) to support stable "Normal" outcomes.


Low Priority: 

•	Monitor seasonal fever trends (e.g., spring's 33 cases) for "Normal" diagnoses through optional wellness check-ins to maintain stability. 

•	Encourage long-term habit tracking for lower-risk ages (e.g., Age 36 at 2.30%) to sustain positive patterns.

ANALYSIS: Diagnosis (Altered)


High Priority: 


•	Prioritise urgent interventions for Age 30 (58.33% alcohol frequency) in "Altered" diagnoses to address potential compounding risks from high consumption and sedentary habits. 

•	Initiate immediate support for trauma-affected individuals ("Yes" trauma, 3 fever counts) to mitigate fever escalation.

Medium Priority:


•	Encourage surgical follow-ups for "Altered" cases with interventions (7 cases) to mitigate fever-related complications, especially in fall (6 cases). 

•	Promote activity adjustments for high sitters (e.g., 9 hours, 16 cases) to reduce risks in "Altered" diagnoses.

Low Priority: 


•	Explore long-term lifestyle education for lower-risk groups (e.g., Ages 27 and 35) to prevent shifts toward "Altered" diagnoses through optional community programs. 

•	Monitor minimal fever seasons (e.g., summer, 1 case) for "Altered" cases as a baseline for gradual improvements.

ANALYSIS: Surgical Intervention (No)


High Priority: 

•	Focus on alcohol reduction for peak groups like Age 28 (36.73%) without surgical interventions to prevent fever spikes (e.g., spring's 17 cases) in "Normal" diagnoses. 

•	Provide immediate trauma support for "Yes" trauma cases (16 fever counts in "Normal") to address elevated risks.

Medium Priority: 


•	Advise activity breaks for high sitters (e.g., 9 hours, 16 cases) in non-intervention groups to support "Normal" outcomes and reduce trauma-linked fevers (16 cases). 

•	Develop fever tracking protocols for fall (15 cases) to maintain stability.

Low Priority: 


•	Consider optional seasonal awareness campaigns (e.g., winter's 14 fevers) for those without surgeries to enhance long-term health maintenance. 

•	Encourage habit education for underrepresented ages (e.g., Age 34 at 2.04%) to promote sustained wellness.

ANALYSIS: Surgical Intervention (Yes)


High Priority: 


•	Provide targeted post-surgical support for Age 30 (30.00% alcohol frequency) with interventions to manage high fever risks (e.g., spring's 20 cases) in "Normal" diagnoses. 

•	Offer urgent rehabilitation for trauma cases ("Yes" trauma, 25 fever counts) to prevent complications.

Medium Priority: 


•	Integrate trauma counselling for those with "Yes" trauma (25 fever counts) post-surgery to address elevated fevers and support recovery. 

•	Recommend mobility programs for high-sitting groups (e.g., 9 hours, 16 cases) to aid healing.

Low Priority: 


•	Promote gradual habit changes (e.g., reducing sitting to 5 hours, 16 cases) for surgical patients as an optional step for sustained wellness.

•	Monitor low-fever seasons (e.g., summer, 1 case) for long-term recovery insights.

ANALYSIS: Season (Fall)


High Priority: 


•	Address fall fever peaks (30 cases) with immediate hygiene protocols for high-alcohol groups like Age 30 (36.67%) to prevent "Normal" diagnosis complications. 

•	Prioritise fever management for trauma cases ("Yes" trauma, 15 fever counts in "Normal") to reduce risks.

Medium Priority: 


•	Encourage mobility for prolonged sitters (e.g., 9 hours, 16 cases) during fall to reduce trauma-linked fevers (15 cases in "Normal"). 

•	Support surgical follow-ups for "Normal" cases (11 with "Yes") to maintain health.

Low Priority: 


•	Offer optional seasonal education on alcohol moderation for underrepresented ages (e.g., Age 35 at 3.33%) to support long-term fall health. 

•	Promote general wellness tracking for low-trauma groups ("No" trauma, 13 fever counts) as a preventive measure.

ANALYSIS: Season (Spring)


High Priority: 


•	Combat spring fever surges (37 cases) with urgent vaccination drives for frequent drinkers like Age 28 (21.62%) to safeguard "Normal" diagnoses. 

•	Provide immediate trauma interventions for "Yes" trauma cases (21 fever counts in "Normal") to control risks.

Medium Priority: 


•	Promote active breaks for high-sitting groups (e.g., 9 hours, 16 cases) in spring to mitigate trauma-related fevers (21 cases in "Normal"). 

•	Encourage surgical awareness for "Altered" cases (19 with "Yes") to improve outcomes.

Low Priority: 


•	Explore optional lifestyle workshops for lower-frequency ages (e.g., Age 34 at 2.70%) to enhance spring wellness over time. 

•	Monitor minimal trauma groups ("No" trauma, 13 fever counts) for long-term preventive strategies.

13. Conclusion:

    
This analysis of the Dream Fertility Clinic dataset for 2022 has illuminated critical risk factors and patterns influencing fertility diagnoses, transforming raw patient data into actionable health insights. Key findings reveal that sedentary behaviour peaks at age 30 (average 20.2 hours/day), strongly correlating with higher alcohol consumption frequencies, particularly among ages 28 (28.28%) and 30 (26.26%), and contributing to "Altered" diagnoses. Surgical interventions showed a slight tilt toward "Normal" outcomes (43 vs. 44 cases without), yet compounded risks from trauma, fevers (peaking at 37 in spring), and smoking (87 counts in "Normal" vs. 12 in "Altered") underscore the need for holistic interventions. Seasonal trends, such as elevated fevers in spring and fall, further highlight environmental moderators on lifestyle impacts.
By identifying high-risk profiles, e.g., frequent drinkers with prolonged sitting, trauma survivors with fever histories, the study equips stakeholders with targeted strategies: age-specific sedentary reduction programs, seasonal fever prevention, post-surgical monitoring, and smoking cessation initiatives. These evidence-based recommendations promise to shift more cases toward "Normal" diagnoses, optimise resource allocation, lower treatment costs, and elevate patient outcomes. This work demonstrates the power of data-driven analysis in preventive fertility care. Future expansions could incorporate longitudinal tracking, advanced modelling (e.g., via Python/R), or additional variables like BMI and stress levels to refine predictions and foster resilient health trajectories at Dream Fertility Clinic.


13. References: Kaggle.com (Fertility Dataset CSV file, accessed 2022 data for analysis).



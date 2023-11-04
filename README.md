# Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning
Predicting Employee Attrition Using Machine Learning

# Background and Objective
Human resources (HR) are the primary assets that need to be effectively managed by companies to achieve their business objectives efficiently. In this opportunity, I will be addressing an issue regarding the human resources within the company. My focus is to understand how to retain employees in the current company, which can result in the swelling of costs for recruiting and training new hires. By identifying the key factors that cause employees to not feel engaged, the company can promptly address these issues by creating relevant programs tailored to the employees' concerns.

# Scope of problem
The problem at hand involves the development of a machine learning system to predict employees who are at risk of leaving their current position. This predictive model will be based on specific characteristics or features associated with employees' behavior, performance, and other relevant factors within the organization. The goal is to identify these "at-risk" employees early in order to implement targeted programs or interventions to retain them within the organization.

# Data



# Data Preprocessing
1. The dataset has 287 records and 25 features
2. Handling missing values ​will be carried out on Mode in IkutProgramLOP, AlasanResign, JumlahKetidakhadiran, SkorKepuasanPegawai, JumlahKeikutsertaanProjek, JumlahKeterlambatanSebulanTerakhir Features
3. SkorKepuasanPegawai, JumlahKeikutsertaanProjek,JumlahKeterlambatanSebulanTerakhir, JumlahKetidakhadiran, IkutProgramLOP can be change to INT64
4. TanggalLahir, TanggalHiring, TanggalPenilaianKaryawan, TanggalResign can be change to DateFrame
5. The phrase "yes" in "PernahBekerja" can be changed to 1
6. The phrase "-" in "StatusPernikahan" can be changed to "Lainnya"
7. The phrase 'Product Design (UI & UX)' in "AlasanResign" can be changed into modus in "AlasanResign"
8. Adding new features: TanggalLahir, TanggalHiring, TanggalPenilaianKaryawan and TanggalResign to extract the year.
9. Creating a new feature where if the ResignationDate is null, it represents 'no,' while if there is a date, it signifies 'yes.'
10. The feature that will be deleted is because it only contains 1 data :PernahBekerja



# Data Analysis
## Annual Report on Employee Number Changes

![download (7)](https://github.com/pwirap/-Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/assets/99533745/d4efddee-104c-4ab8-8491-678ab5b89f58)

In 2011, the year witnessed the highest number of new employees joining the company compared to those who left, totaling 76. However, in 2015, a significant surge in employee resignations occurred, necessitating further analysis to understand the underlying reasons. Subsequently, from 2015 onwards, there was a continuous decline in the number of employees, reaching its peak in 2018 when a substantial number of employees departed, far outnumbering the new recruits. During this period, the company faced challenging conditions, highlighting the urgent need for self-improvement to ensure the sustainability of long-term strategic goals without encountering further complications.


## Resign Reason Analysis for Employee Attrition Management Strategy



The data illustrates the overall percentage of employees in each existing department compared to those who have resigned up to the year 2018. Notably, employees in roles such as DevOps Engineer, Digital Product Manager, Machine Learning Engineer, Product Design, Scrum Master, and Software Architect have not submitted their resignations. However, the Data Analysts department stands out with the highest resignation rate, where as much as 50% of its employees have resigned. It is crucial to investigate the underlying reasons for this significant turnover among Data Analysts.

## Resign Reason Analysis for Employee Attrition Management Strategy

The graph illustrates a correlation between the reasons for resigning and the performance of data analysts, with all resigning data analyst employees being recent graduates. Interestingly, despite their outstanding performance, the presence of a toxic culture compels employees to resign, highlighting the need for an in-depth examination of why data analyst employees perceive the work environment as toxic.

## Feature Selection
By using Mutual Information, we get only certain features that have an important role in the target, namely "StatusPernikahan" , "StatusKepegawaian", "Pekerjaan" , "AsalDaerah" , "HiringPlatform" , "AlasanResign"

## Model Machine Learning
The following is an evaluation matrix table on several machine learning models that have been tested


We are focusing on Recall, and XGBoost emerges as the best model due to the evaluation matrix in both the training and testing phases not differing significantly and doesn't make Overfitting.

#Summary
1. Feature Selected : "StatusPernikahan" , "StatusKepegawaian", "Pekerjaan" , "AsalDaerah" , "HiringPlatform" , "AlasanResign"
2. Model Machine learning selected : XGBoost
3. Feature Important : AlasanResign

"Grafik Resign"




From the adjacent chart, it can be concluded that the most common reasons for resignation are associated with working hours, career change, uncertainty in career advancement, and the inability to work remotely.

# Business Recommendation

1. **Flexible Working Hours**: To address the issue of resignations related to working hours, consider implementing flexible working hours or remote work options where feasible. This can improve work-life balance and employee satisfaction.
2. **Career Development and Clarity**: Provide employees with clear paths for career advancement within the organization. Offer training, mentorship, and opportunities for skill development to help them progress in their careers.
3. **Remote Work Options**: Explore the possibility of allowing employees to work remotely, at least in part. This can be particularly important for those who value the flexibility of working from different locations.
4. **Skills Development**: Invest in training and development programs to help employees acquire the skills they need to advance within the company. This can boost loyalty and engagement.






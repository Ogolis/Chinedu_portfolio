# Healthcare Insurance Analysis

### Project overview

The project aims to investigate the effect sex, age and region has on Health insurance Charges

![Health Insurance](https://github.com/Ogolis/Healthcare-Insurance/assets/136832743/3f41231d-a0bb-4d95-932f-f9d4c06375dd)


### Data Sources:

The data was openly sourced from Kaggle Healthcare Insurance Dataset

### Tools:

Excel, MS SQL and Power Bi were used in cleaning and analyzing the data

### Data Cleaning/Preparation
In the initial data preparation phase, we performed the following tasks:

Data loading and inspection.
Handling missing values.
Data cleaning and formatting.

### Exploratory data analysis:
Exploratory data analysis seeked to answer the following questions:

1) What is the effect age has on Healthcare Insurance cost?
2) What is the effect sex has on Healthcare Insurance cost?
3) What is the effect region has on Healthcare Insurance cost?

### Data Analysis:

The data was analyzed in MS SQL using the following:
First I loaded the Insurance dataset into the Portfolioproject Database on MS SQL

`SELECT
	*
FROM
	Portfolioproject..insurance`

Let's look at the average cost of health care insurance by age

`SELECT
	age, ROUND(AVG(charges),2) AS AverageInsuranceCost
FROM
	Portfolioproject..insurance
GROUP BY
	age
ORDER BY
	age DESC`

Let's look at the average cost of health care insurance by sex

`SELECT
	sex, ROUND(AVG(charges),2) AS AverageInsuranceCost
FROM
	Portfolioproject..insurance
GROUP BY
	sex`

Average cost of healthcare charges per region

`SELECT
	region, ROUND(AVG(charges),2) AS AverageInsuranceCost
FROM
	Portfolioproject..insurance
GROUP BY
	region`

Effect of BMI on healthcare charges

`SELECT
	BMI, ROUND(AVG(charges),2) AS AverageInsuranceCost
FROM
	Portfolioproject..insurance
GROUP BY
	BMI`

### Results/Findings
The result/findings are summarized below:
1) A correlation exists between age and health insurance charges. This is evidenced by the scatter plot diagram
showing the relationship between Age and Average Insurance Charges.
2) Males on average are spending more on health insurance charges than women across different sub categories such as region and age.
3) Individuals from the south east are spending more on health care compared to any other region.

### Recommendations
Based on my findings, I recommend the following:
1) Measures should be put into place to cushion the cost of health insurance charges for elderly citizens, especially those beyond the retirement age. This is quite important as the risk for certain health conditions such as high blood pressure and stroke tends to be higher for elderly citizens.
2) It should be looked into why Males on average pay more than Female Patients. Are there certain procedures that cost more? are there certain health conditions Males are more predisposed to than Females?
3) Implement a strategy to reduce the cost of Health care Insurance for residents from the south east region.



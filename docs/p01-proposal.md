# Trends in U.S. Minimum Wage from 1968-2020

**Project Code Name**:<br>AMBA

**Authors**:<br>
Fatima Alsinai: alsinf@uw.edu<br>
Sarah Mun: sarahhm@uw.edu<br>
Vianne Buinguyen: vianneb@uw.edu<br>
Victor Ahn: victor971125@uw.edu<br>

**Affiliation**:<br>
INFO-201: Technical Foundations of Informatics - The Information School - University of Washington

**Date**:<br>
Winter 2022

## Abstract
Our main question for this data set is "How does the consumer price index change relative to state wage?". This question is particularly important because it tells us whether or not employees are making enough money to purchase goods and necessities. To address this question, we will use `R` to extract data from the [Minimum Wage dataset](../data/Minimum-Wage-Data.csv) that we obtained from the Kaggle website, and write our reports in Atom using Markdown.

_**Keywords**: State minimum wage, federal minimum wage, consumer price index, living wage_

## Introduction
This project focuses on assessing whether the current state wage in Washington state is high enough for workers to purchase goods. The dataset used in this project is titled _U.S. Minimum Wage by State from 1968 to 2020_. In order to perform our analysis of this data, we will extract the consumer price index (CPI) and state wage from the data set. Comparing the changes of these two values over time will allow us to find out whether the state wage has increased enough to catch up with the changes in the consumer price index. If the ratio between the minimum wage and CPI is greater than 1, then the goods are relatively cheaper than before. If the ratio is equal to 1, then the minimum wage has increased at the same rate as the CPI. If it is lower than 1, it means that the goods are more expensive than before and minimum wage should be higher.

## Design Situation
### Project Framing
The question we want to address is whether or not state and federal minimum wages have been sufficient enough to live on. This involves analyzing past state and federal minimum wages and comparing them to the average value of the Consumer Price Index at the time. The issue has social, economic, and governmental implications. It is a social issue because the minimum wage controls citizens’ quality of life and poverty levels. It is an economic issue because the minimum wage affects employment levels and consumer spending power and demand for goods–all of which are factors that contribute to the economy’s growth and decline. Lastly, it is a governmental issue because federal and state governments hold the power to change the minimum wage.

### Human values
The main human values connected to our project are a concern for citizens' wellbeing and quality of life, and an attempt to achieve social justice by drawing conclusions that may decrease economic inequality and bridge the poverty gap. As college students, we understand the financial pressure of struggling to make ends meet while working minimum wage jobs. However, raising the minimum wage has been a long-debated issue. According to a Pew Research Center survey conducted in April 2021, about 6 in 10 U.S. adults (62%) favored raising the federal minimum wage, while 4 in 10 (38%) opposed the proposal (Pew Research Center). "Proponents of raising the minimum wage argue that the current federal rate is too low and not commensurate with the rising cost of living...Opponents, however, worry that an increase will place an undue burden on business owners, prompting layoffs and greater unemployment" (National Conference of State Legislatures).

### Direct and Indirect Stakeholders
The direct stakeholders of our topic of interest are working class Americans, who will be most affected by any changes to the minimum wage. This group primarily consists of people who hold jobs which “provide low pay, require limited skill, or physical labor” (Investopedia). This group’s primary motivation is to earn a living wage to cover necessities such as food, rent, and healthcare for themselves and their dependents. Indirect stakeholders include policymakers. Although they are not affected directly by minimum wage laws, they still hold the power to change the minimum wage.

### Benefits and harms
Changes made to the minimum wage, particularly raising it, comes with benefits and consequences. The most obvious benefit would be lifting low-wage workers and their families out of poverty. According to the nonpartisan Congressional Budget Office (CBO), increasing the minimum wage to $15 could lift 900,000 people out of poverty. However, increasing the minimum wage means increasing the cost of hiring a worker – which may not be sustainable for smaller businesses. The CBO estimates that "raising the federal minimum wage to $15 an hour by 2025 would increase wages for at least 17 million people, but also put 1.4 million Americans out of work" (NPR). The CBO adds, "Young, less educated people would account for a disproportionate share of those reductions in employment" (NPR).

## Research Questions
1. How has the US states' minimum wage changed over time?


2. How has the federal minimum wage changed compared to consumer price index over time?


3. How does the ratio of the US states' minimum wage to consumer price index change over time?


In order to find out whether the minimum wages increased, there are questions to be asked. First, it is important to find out how Washington's state wage has changed over time. By doing so, we are able to compare it with the CPI. Besides state wage, we also have to question the change of  Federal wage over time. As we did for state wage, we should also try to compare Federal wage with CPI. These two different comparisons will give us a complete understanding over the ratio of minimum wage and the consumer price index.

## The Dataset
 - **Dataset size and complexity**: [Our dataset](https://www.kaggle.com/lislejoem/us-minimum-wage-by-state-from-1968-to-2017) consists of one file, comprised of 2,863 rows and 15 columns.  


 - **What is represented in the data?**: U.S. state and federal minimum wages from 1968 to 2020


 - **What is an observation? What variables are included (an excluded)?**: An observation contains the following variables


  | **Observation** | **Description** |
  |-----------------|-----------------|
  |Year | The year of the data |
  |State | The state or territory data |
  |State.Minimum.Wage | The state's minimum wage starting on January 1 |
  |State.Minimum.Wage.2020.Dollars | The state minimum wage converted to 2020 dollars |
  |Federal.Minimum.Wage | The federal minimum wage starting January 1 |
  Federal.Minimum.Wage.2020.Dollars | The federal minimum wage converted to 2020 dollars |
  |Effective.Minimum.Wage | The minimum wage that is enforced in the state on January 1. This value would equal the federal minimum wage if the state minimum wage is lower than the federal minimum wage |
  |Effective.Minimum.Wage.2020.Dollars | The effective minimum wage converted to 2020 dollars |
  |CPI.Average | The average value of the consumer price index. The consumer price index is a "measure of the average change over time in the prices paid by urban consumers for a market basket of goods and services" (U.S. Bureau of Labor Statistics). |
  |Department.Of.Labor.Uncleaned.Data | The unclean, scraped value from the United States Department of Labor's website. |
  |Department.Of.Labor.Cleaned.Low.Value | The state’s lowest enforced minimum wage on January 1. Some states enforce different minimum wage laws depending on the size of the business, with smaller businesses typically having lower minimum wage requirements. |
  |Department.Of.Cleaned.Low.Value.2020.Dollars | The state's lowest enforced minimum wage in 2020 dollars |
  |Department.Of.Labor.Cleaned.High.Value | The state's highest enforced minimum wage of January 1 |
  |Department.Of.Labor.Cleaned.High.Value.2020.Dollars | The state's highest enforced minimum wage in 2020 dollars |
  |Footnote | The footnote provided on the United States Department of Labor's website, if any |  

<br>
- **Who collected the data? For what purpose? How was the data collection effort funded? Who is likely to benefit from the data or make money?**: This dataset was put together by Kaggle contributor, Lislejoem, who cleaned and aggregated data that was scraped from the [United States Department of Labor's table of minimum wage by state](https://www.dol.gov/agencies/whd/state/minimum-wage/history). The Kaggle dataset contains state and federal minimum wage data from 1968 to 2020 and was last updated on December 31, 2020. Lislejoem claims to have put this together because "While looking online for a clean dataset for minimum wage data by state, I was having trouble finding one. I decided to create one myself and provide it to the community" (Lislejoem). This data collection effort was not funded and was done purely due to the recognition of the need for a comprehensive clean dataset for minimum wage data by state. While the creator of this dataset will not make money, working class Americans may benefit from efforts to raise minimum wage standards that may result from the analysis of this dataset.


- **How was the data validated and held secure? Is it credible and trustworthy?**: The original data comes from the United States Department of Labor. Since this is a cabinet-level department of the United States federal government that is responsible for wage a hour standards, we can be sure its a minimum wage data is the most accurate and valid form available. Additionally, we can be sure that this data was held secure since the federal government's data infrastructure is strongly protected by the Cyber & Infrastructure Security Agency, meaning federal government data breach incidents rarely occur.


- **How did you obtain the data? Do you credit the source of the data?**: We obtained the dataset through Kaggle. It is cited in our References section.

## Expected Implications
Based on our research questions, we believe that policymakers would be most affected by our data set and analysis. Our project seeks to answer the question of how minimum wage affects an individual’s ability to afford basic goods and necessities. Comparing the federal and state wages may push policymakers to reevaluate what their minimum wages should be in order to make these goods accessible. Especially in states with minimum wages below the federal standard, this would be an important consideration for citizens who currently cannot afford these goods because of the low standard. Technologists and designers may also be affected by our data as professionals who create solutions for a wide range of audiences. Understanding how consumers are affected by low minimum wages may help these professionals find ways to create more accessible products and solutions for those in lower income areas.

## Limitations
Although the data in this database shows us the correlation between the minimum wage increase and the average value of the Consumer Price Index in a year, there are limitations to the data which must be recognized. There is no data on the types of products the population purchases or information about the products’ cost overtime. Thus, we can’t compare how competitive the labor market is since we do not have the weight of each category in the basket. Also, there is no data about the job market which limits the use of the data for the purposes of analyzing employment trends. We also can’t use the data to determine the negative implications, such as the amount of jobs lost/gained or inflation due to the increase in minimum wage. Additionally, we are unable to identify the change in employment rates of one state relative to other states.

## References
Changes in basic minimum wages in non-farm employment under state law: Selected years 1968 to 2021. (n.d.). Dol.Gov. Retrieved February 4, 2022, from https://www.dol.gov/agencies/whd/state/minimum-wage/history

CPI home. (2017, October 11). Bls.Gov. https://www.bls.gov/cpi/

Kenton, W. (2021, December 30). Working Class. Investopedia. https://www.investopedia.com/terms/w/working-class.asp

Lislejoem. (n.d.). US Minimum Wage by state from 1968 to 2020 [Data set].

Most Americans support a $15 federal minimum wage. (2021, April 22). Pew Research Center. https://www.pewresearch.org/fact-tank/2021/04/22/most-americans-support-a-15-federal-minimum-wage/

Saige Draeger, L. K. (n.d.). Increasing the minimum wage. Ncsl.Org. Retrieved February 4, 2022, from https://www.ncsl.org/research/labor-and-employment/increasing-the-minimum-wage.aspx

Selyukh, A. (2021, February 8). $15 minimum wage would reduce poverty but cost jobs, CBO says. NPR. https://www.npr.org/2021/02/08/965483266/-15-minimum-wage-would-reduce-poverty-but-cost-jobs-cbo-says

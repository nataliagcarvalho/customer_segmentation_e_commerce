# Customer Segmentation in Ecommerce

<a href="https://datastudio.google.com/reporting/1311a992-20bb-4d8d-abb5-839e75a2ef04">Dashboard in Google Data Studio</a>

<a href="https://docs.google.com/spreadsheets/d/1tmJglsLmb90C0JMNA9EaKHq_0lnsSJMLap1i_muuwtU/edit#gid=2011282344">Exploratory Analysis</a>

***

This is a project from the Laboratoria & IBM Data Analyst Certification.

The idea of this project is to do a descriptive analysis to show to the Ecommerce's CEO how good (or not) the sales are going, to measure the retention and churn rates by cohort and to do a customer segmentation applying the RFM metodology considering also de Pareto's Principle in order to concentrate the efforts on the "right" customers.

The ecommerce (UK Merch) is a young company that sells wholesale clothing with a very competitive price. Its clients are small clothes business that fill their stocks buying from it. They have clients from many countries but their main ones are from UK. 

***

# Dataset

This dataset contains 6 columns with the following informations: recipe number, recipe date, client id, country, quantity and value.

You can find it <a href="https://www.kaggle.com/datasets/datacertlaboratoria/projeto-3-segmentao-de-clientes-no-ecommerce">here</a>.

***

# Data pre-processing

This dataset doesn't have good quality. It's full of duplicated and empty data as also negative values.
In order to achieve better quality, I have deleted all the duplicated data in google sheets.
The next step was to do a query to remove all the empty data and negative value: 
```
=QUERY('base-de-dados'!$A:$F, "SELECT * WHERE C IS NOT NULL AND F >= 0  ")
```
I've created the clean-base and added the columns year-month considering the cohort and also a column to identify if the client belongs to UK or not.

***

# Exploratory Analysis

At this point, I did an exploratory analysis to do the sales metrics analysis.

![Captura de Tela (928)](https://user-images.githubusercontent.com/106877571/177341128-da81c112-c77c-481d-aab8-001d8738db82.png)

Analyzing the number of emited recipes, we can see that the main client is in UK, which represents 89,82% of emited recipes.
Once we compare the emited recipes in UK and ohter countries in a line chart during the period of 1 year, we can take other great insight.

![Captura de Tela (929)](https://user-images.githubusercontent.com/106877571/177341812-28fcf8ab-29a0-48ab-90e0-260c4cc3d6ea.png)

In 2021 November, we see a peak of emited recipes for both (UK and other countries), which can be because any specific marketing campaign that the company had launched but also because of the Black Friday season or even pre Christmas sales. However, we notice that it has a significant decrease in December. 
In order to better understand this number, I took another look at the dataset and could see that it has a fail once it was only registered until December 9th. Because of this, we missed a great opportunity to have a better analyze of this period.

![Captura de Tela (930)](https://user-images.githubusercontent.com/106877571/177343652-40d216de-264b-4df5-bf78-8b298bb8759b.png)

Another important analyze was the revenue of each country. As we could already see, UK is the country buyer leader. However, we see that the medium ticket is not the highest. While Netherlands, Singapore, Australia, EIRE and Switzerland have the hightest medium ticket, which means that they are spending more per purchase. And through this analysis, I've built this chart where we can better see the medium ticker per country, where we have Netherlands with the hightest one:

![Captura de Tela (931)](https://user-images.githubusercontent.com/106877571/177346868-c3c6904e-829a-40d6-bbbc-60f0a0201f90.png)

Something that is also important for the business intelligence is to understand if the company is achieving new clients. In order to find out this, I've counted the new clients per month and extrapolated these numbers to a chart:

![Captura de Tela (932)](https://user-images.githubusercontent.com/106877571/177348712-d0f39558-cca8-42a9-b2af-63451378628a.png)

![Captura de Tela (933)](https://user-images.githubusercontent.com/106877571/177348959-95000bf8-70e6-4366-a230-d64e94fea165.png)

Completing the analyze about the sales at 2021 November, we can see that the sales were higher also because a great number of clientes were achieved.

***

# Cohorts Analyzes


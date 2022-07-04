# Customer Segmentation in Ecommerce

<a href="https://datastudio.google.com/reporting/1311a992-20bb-4d8d-abb5-839e75a2ef04">Dashboard in Google Data Studio</a>

<a href="https://docs.google.com/spreadsheets/d/1tmJglsLmb90C0JMNA9EaKHq_0lnsSJMLap1i_muuwtU/edit#gid=2011282344">Descriptive Analysis</a>

***

This is a project from the Laboratoria & IBM Certification.

The idea of this project is to do a descriptive analysis to show to the Ecommerce's CEO how good (or not) the sales are going, to measure the retention and churn rates by cohort and to do a customer segmentation applying the RFM metodology considering also de Pareto's Principle in order to concentrate the efforts on the "right" customers.

The ecommerce (UK Merch) is a young company that sells wholesale clothing with a very competitive price. Its clients are small clothes business that fill their stocks buying from it. They have clients from many countries but their main ones are from UK. 

***

# Dataset

This dataset contains 6 columns with the following informations: recipe number, recipe date, client id, country, quantity and value.

***

# Data pre-processing

This dataset doesn't have good quality. It's full of duplicated and empty data as also negative values.
In order to achieve better quality, I have deleted all the duplicated data in google sheets.
The next step was to do a query to remove all the empty data and negative value: 
   =QUERY('base-de-dados'!$A:$F, "SELECT * WHERE C IS NOT NULL AND F >= 0  ")

I've created the clean-base and added the columns year-month considering the cohort and also a column to identify if the client belongs to UK or not.

***

#

# (Dataset Exploration on Loan Data from Prosper)
## by (Bright Akachi Daniel)


## Dataset

> Loan Data from Prosper contains 113,937 loan transactions with 81 variables on each loan, including loan original amount,various features of borrowers, current loan status and many others. This dataset is available at
https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv, for a better understanding of this dataset, the intepretations of the 81 variables is available at https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0

## Summary of Findings

                                 Distribution of Selected Variables
> Loan Status: I found out that the Current loan is the most frequent followed by Completed, Chargedoff, Defaulted Past due(1-15 days), etc. This analysis will focus on the top five most occurring statuses.
Loan Original Amount: The distribution is multimodal, and shows a right skewness. More loans were collected at amounts between $0-12,000. Using a log transformation on both axes one at a time, it can be seen that; (a) X-axis log transformation shows that more loans were collected between (S1000-10000) (b) Y-axis log transformation shows more skewness to the right and multimodal distribution compared to X-axis log transformation.
Boolean Variables: 50.4% of borrowers are homeowners,11.2% are currently in a group,92.4% are with verifiable income source while 49.6% are not homeowners,88.8% are not currently in a group and 7.6% don't have a verifiable income source.
Occupation: there are a lot of categories in this variable, so I visualized the 10 most occurring in this dataset to streamline further analysis.
Employment Status: As I expected, this follows an order that shows that most borrowers are actively employed. This can be a result of the company giving loans to those that are actively employed than those that are inactive. 
Prosper Score: the distribution does not follow a particular pattern but scores of 4,6, and 8 occurred mostly.

                                    Observed Relationships
Prosper score gave the lowest risk score(high prosper score) to borrowers who are homeowners, currently in a group, and with verifiable sources of income as displayed in the bar and pie charts.
Prosper score gave the lowest risk ranking to borrowers that have completed their loan followed by those who are at the final payment stage. Those whose payday had past by 120 days were given the highest risk rank, defaulters at all stages also received a higher risk rankingas shown in the barplot. Based on the above, I recommend that Prosper Score was effective and meets its target.
Loan Status: Borrowers with verifiable sources of income completed their loans while a few defaulted. Those who are currently in a group completed their loan compared to those that are not while those that are not homeowners completed their loan compared to those who are as seen on the clustered bar chart.

          Loan Original Amount Vs Boolean Values

Borrowers that are homeowners, with a verifiable sources of income collected higher amounts of the loan compared to their opposites. This can result from the company seeing them as being creditworthy or giving them preference over their opposite pairs. Borrowers who are not in a group collected a higher amount of loans compared to those that are not. This can  result from those in a group getting the money needed from the groups they belong to. (boxplot)

           Loan Original Amount Vs Other Variables

Loan Status: Current borrowers have the highest amount of loan while almost the same amount was given to those with completed, charged off, and defaulters.
Occupation: Executives collected a higher amount of loan than any of the six occupations considered. Computer Programmers, Analysts, and Professionals collected almost the same amount.
Employment status: As expected, people who are actively employed collected a higher amount than those that are passively and inactively employed. (boxplot and violin plot)

Finally, there is a linear relationship between Loan original amount, Prosper score, and the boolean variable being considered, following the same trend as what was observed in the bivariate plots. There is also a linear relationship between the Loan original amount, Prosper score, and the loan statuses been considered, this is more pronounced in the Current status as shown in the scatterplot. A linear relationship exists between Loan original amount, Prosper score, and all categories of Occupations considered as shown in the scatterplots. A linear relationship exists between the Loan original amount, Prosper score, and the employment statuses of Self-employed, employed, other, and not employed. A constant relationship exists between the Loan original amount, Prosper score, and the employment statuses of full-time and retired while there is a negative relationship between the Loan original amount, Prosper score, and part-time employment status. This didn't go as expected, I was expecting a negative correlation to exist between the Loan original amount, Prosper score, and the employment status of Not employed as we have seen in previous trends.


## Key Insights for Presentation

> For this project, I focused on the borrowers' features(being a home owner,having a verifiable source of income and currently being in a group) to determine their credit worthiness. I compared these attributes of the borrowers to the Loan Statues, Prosper Score(risk ranking from 1-10) and the Original amount of loan collected.
    I started by looking at the distribution of theses variables individually then moved to comparing them pairs after which I compared them in three's.
   Athough no system is 100% efficient as a saying goes but these attributes are good and effective in determimng the credit worthiness of a borrower. I strongly recommend that care should be taken while using these features because borrowers' behaviour meant differ.
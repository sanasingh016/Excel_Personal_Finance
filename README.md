# Personal Finance Analysis Using Excel 
<img align="right" alt="Client Financial Analysis with Excel" width="1000" height = "500" src="https://github.com/sanasingh016/Personal_Finance_Analysis/blob/abd6a3d8c9091ee6a7059e2d3a14cf6c86fc3d1b/Final%20Result.png">

**Problem Statement**

Using the client's financial data over a period of 20.4 Months:
- Find out the total expenses incurred, total income, amount of money spent in relation to the budget set, and the total sum of transactions done through each account.
- Produce everything the client needs to know about her finances.
- Provide reccomendations to the client which will allow her to be mindful about her future spending.

**Data Sourcing**

The Dataset used for this analysis was found on kaggle by the user @/bukolafatunde (https://www.kaggle.com/datasets/bukolafatunde/personal-finance/data) and is available at

-<a href="https://github.com/sanasingh016/Personal_Finance_Analysis/blob/abd6a3d8c9091ee6a7059e2d3a14cf6c86fc3d1b/archive.zip">Raw Data</a>

In this dashboard, data is pulled from income and expense statements from the  `Personal Expenses` spreadsheet that had been combined into one from 1/1/2018 to 9/30/2019, represented in `807 rows` and `7 columns`. Apart from this, I also used the monthly `Budget` spreadsheet that had `20 rows` and `3 columns` and muliplied it into 20.4 Months to find the total budget.

**Steps**

- I made sure my spreadsheet included columns for the Categories, Total Amount Spent, Total Budget, and the Remaining Amount.
- I used the exact formula `=SUMIFS(Table1[Amount],Table1[Category],Final!B20,Table1[Date],">="&Final!$C$6,Table1[Date],"<="&Final!$C$7)` to ensure the total amount of expenditure incurred in each category can be changed if the client decides to select a different set of dates.
- Added the Budget and subtracted the same with the Amount Earned. Since the raw data included Credit Card Payments in both the debit and credit sections, Creating a `pivot chart` with the `Transaction Type` and `Category` under Rows and `Sum of Amount` under Values allowed me to clearly differentiate between the types of transactions (e.g., debit vs. credit) and categorize them accordingly.
- Following this, `Conditional Formatting` the subtracted result allowed me to show the cells that were exceeding the budget in Red and the ones below the budget in Green.
- The final step for this section was completed by calculating the total amount spent and the total amount over/under the budget. I then created charts to help the client visualize the data better.

- Then by using pivot tables again I found out the total sum of transactions done through each account and then used a pie chart to visualize my findings.
- I then worked on the income earned section and used the formula =SUMIF(A:A, "Credit", B:B) to sum all Credit transactions.
- I copied the results of my calculations (total expenses, total income, budget comparison, and total transactions per account) to a new sheet for a clear summary view.

**Data Analysis**

Measures used in visualization are:

- Actual = `SUM(Transactions[Amount])`
- Balance = `SUM(Budget[Amount])`
- Balance = `[Budget]-[Actual]`

With this, we can now say that
- The clients spent `$48,024` over the budget
- The client spent a total amount of `$96,005`
- The client has a balance of `$28,264`

**Insights**

- The client has spent the highest amount on `Credit Card Payments`
- The client also spent `$19,000` on Home improvements which was an amount far greater than the budget. However since this can be considered a one time investment it does not affect the client that greatly.
- 80% of the transactions were done through a checking account. 

**Recomendations**

Since the client exceeded the budget by $48,024, it's important to review and adjust the budget to better reflect actual spending patterns. Consider allocating a higher budget for categories where overspending occurred, such as Credit Card Payments and Home Improvements. They should regularly update and review financial records to track spending trends and ensure alignment with budget goals. Implement a system for ongoing monitoring and adjustment of the budget as needed.


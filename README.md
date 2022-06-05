## Finances

### Data Analysis Using Power BI
==================================

1. Formula for Total savings

	Total Saving = CALCULATE(SUM(FinData[Value]),FinData[Type]="Savings")
  
2. Formula for Total income

	Total Income = CALCULATE(SUM(FinData[Value]),FinData[Type]="Income")

3. Formula for Total expenses

	Total Expense = CALCULATE(SUM(FinData[Value]),FinData[Type]="Expense")
	
4. Formula for savings%

	Savings % = DIVIDE([Total Saving],[Total Income])

5. Formula for expense%

	Expense % = DIVIDE([Total Expense],[Total Income])
	
6. Formula for income change month on month

	Income Change MoM % = DIVIDE([Total Income],[Income LM])
	
7. Formula for Net worth

	Cumulative Net Worth = 
	CALCULATE (
    Total Saving],
    FILTER (
    ALL ( FinData[Date] ),
    FinData[Date] <= MAX ( (FinData[Date] ) )
    )
	)


exp9:

Revenue percentage = SUM(SalesTable[Revenue])/ (CALCULATE(SUM(SalesTable 
[Revenue]),ALL(SalesTable[Country]))*100) 



FEmale Revenue = CALCULATE(SUM(SalesTable[Revenue]),SalesTable[Customer 
Gender]="F") 
Male Revenue = CALCULATE(SUM(SalesTable[Revenue]),SalesTable[Customer 
Gender]="M")

Avg Revenue per State = SUM(Revenue) / DISTINCTCOUNT(State) 

Profitability = IF(Avg Revenue per State > [Threshold], "Profitable", "Non
Profitable")

exp11:

Employee Count: 
Employee Count = COUNT('Table'[EmployeeID]) 
Attrition Count: 
Attrition Count = CALCULATE(COUNT('Table'[EmployeeID]), 'Table'[Attrition] = 
"Yes") 
Attrition Rate: 
Attrition Rate = DIVIDE([Attrition Count], [Employee Count], 0) 
Active Employees: 
Active Employees = CALCULATE(COUNT('Table'[EmployeeID]), 'Table'[Attrition] = 
"No") 
Average Age: 
Average Age = AVERAGE('Table'[Age]) 

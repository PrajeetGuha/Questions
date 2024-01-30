# Problem Statement - Coding

- DateFormat : "dd/MMM/YYYY" example: 10/Jan/2024

Create a class called **Project** that has following attributes -
- ProjectName : String
- StartDate : DateFormat
- ProposedEndDate : DateFormat
- ProjectOwner : String
- BudgetAllocated : BigInteger
- Department : String

The class should have following methods -
- remainingBudget(budgetExhausted : BigInteger) : BigInteger (calculates the remaining budget = BudgetAllocated - budgetExhausted)
- timeElapsed() : DateFormat (Today's Date - StartDate)
- timeRemaining() : DateFormat (ProposedEndDate - Today's Date)

### Constraints:
- User while giving input will also follow the Date and Currency format so no need to input validate.

### Input format:  
ProjectName  
StartDate  
EndDate  
ProjectOwner  
BudgetAllocated  
Department  
BudgetExhausted  

### Output format:  
remainingBudget  
timeElapsed  
timeRemaining  

### Input - 
```
ABC_Project
10/Jan/2024
30/Mar/2024
ABC_Limited
20000
Software
10000
```
### Output (as per today 27/Jan/2024) - 
```
10000
17
63
```

---

# Problem Statement - SQL

Note: Schema notation is for understanding. The datatype nomenclature may vary from platform to platform.

The schema is as follows - 
| project_id(PK) | project_name | start_date | proposed_end_date | project_owner | budget_allocated | department |
|---------------|-------------|-----------|-----------------|--------------|-----------------|------------|
| Int           | String      | Date      | Date            | String       | Long int        | String     |

The output of your query should give the highest and the lowest budget allocated(sum of all allocations), with the department name to which they are allocated. The output format-
| type                        | department | total_budget_allocated |
|-----------------------------|------------|------------------------|
| IN ("Highest", "Lowest")    | String     | Long int               |

It should have two rows always. (One for highest and one for lowest).

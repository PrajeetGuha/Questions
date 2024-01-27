# Problem Statement - Coding

CurrencyFormat : "$X,XXX,XXX.XX" (thousand separator following American System with always 2 decimal points) example: $10,000,000,00 | $80.00
DateFormat : "dd/MMM/YYYY" example: 10/Jan/2024

Create a class called **Project** that has following attributes -
- ProjectName : String
- StartDate : DateFormat
- ProposedEndDate : DateFormat
- ProjectOwner : String
- BudgetAllocated : CurrencyFormat
- Department : String

The class should have following methods -
- remainingBudget(budgetExhausted : String) : CurrencyFormat (calculates the remaining budget = BudgetAllocated - budgetExhausted)
- timeElapsed() : DateFormat (Today's Date - StartDate)
- timeRemaining() : DateFormat (ProposedEndDate - Today's Date)

Constraints:
- User while giving input will also follow the Date and Currency format so no need to input validate.
- $100,000,000.00 >= Currency >= $0

---

# Problem Statement - SQL

Note: Schema notation is for understanding. The datatype nomenclature may vary from platform to platform.

The schema is as follows - 
| project_id(PK) | project_name | start_date | proposed_end_date | project_owner | budget_allocated | department |
|---------------|-------------|-----------|-----------------|--------------|-----------------|------------|
| Int           | String      | Date      | Date            | String       | Long int        | String     |

The output of your query should give the highest and the lowest budget allocated, with the department name to which they are allocated. The output format-
| type                        | department | totalbudgetallocated |
|-----------------------------|------------|----------------------|
| String("Highest", "Lowest") | String     | Long int             |
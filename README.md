# Banking Transaction Database Testing

## Project Overview
This project focuses on validating banking transaction workflows through manual testing and SQL-based database validation. The objective is to verify transaction accuracy, data consistency, input validation, and appropriate error handling in a demo banking application.

## Objectives
- Validate fund transfers, account balances, and transaction history.
- Design test cases for valid and invalid banking transactions.
- Verify database records using SQL queries.
- Identify defects and document discrepancies between expected and actual results.

## Scope of Testing
- Fund transfers between accounts
- Account balance verification
- Transaction history and statement records
- Insufficient balance and invalid transaction scenarios
- Input validation and error handling
- Database consistency and transaction record verification

## Testing Activities
- **Test Case Design:** Prepare test scenarios covering positive, negative, and boundary conditions.
- **Test Execution:** Execute test cases and record actual results against expected outcomes.
- **Database Testing:** Use SQL queries to verify transaction records and account balances.
- **Defect Reporting:** Document issues with steps to reproduce, expected results, and actual results.
- **Regression Testing:** Re-test affected functionality after fixes, where applicable.

## Technology Stack
- **Testing:** Manual Testing, Functional Testing, Regression Testing
- **Database:** SQL, SQL Server
- **Concepts:** DBMS, Data Validation, Transaction Integrity
- **Documentation:** Microsoft Excel, Test Case Reports, Defect Logs

## Sample Test Scenarios

| Test Scenario | Expected Result |
|---|---|
| Transfer a valid amount between accounts | Transaction is processed and balances are updated correctly |
| Attempt a transfer with insufficient funds | Transaction is rejected with an appropriate message |
| Enter an invalid transfer amount | The system validates or rejects the input |
| View transaction history | Correct transaction details are displayed |
| Verify transaction records using SQL | Stored records match the expected transaction results |

## Project Deliverables
- Test scenarios and test cases
- Test execution records
- SQL validation queries
- Defect reports
- Test summary report

## Key Learnings
- Understanding manual testing techniques and the software testing life cycle.
- Applying SQL queries to validate records and data consistency.
- Testing negative scenarios and transaction error handling.
- Documenting defects and reporting testing outcomes.

## Application Under Test
ParaBank Demo Banking Application: https://parabank.parasoft.com/parabank/

## Disclaimer
This project is intended for educational purposes. Test results and defect reports should reflect actual test execution. SQL Server validation requires a corresponding database or test dataset; do not claim backend database testing unless it has been performed.

## Author
Barin Ghosh

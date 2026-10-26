# Test Plan – ParaBank Manual Testing Project

## 1. Objective

Validate the functional behavior, navigation, input validation, transaction workflows, and basic usability of the ParaBank demo banking application through comprehensive manual testing.

## 2. Test Types

- **Functional Testing** - Verify all features work as expected
- **Smoke Testing** - Quick validation of critical paths
- **Sanity Testing** - Validate core functionality after changes
- **Regression Testing** - Ensure no new issues after fixes
- **Negative Testing** - Test error handling and invalid inputs
- **Boundary Value Testing** - Test limits and edge cases
- **Input Validation Testing** - Verify field validation rules
- **UI/Navigation Testing** - Verify page layout and usability
- **Compatibility Testing** - Test across different browsers
- **API/Service Testing** - Basic endpoint availability checks

## 3. Scope - In Scope

All customer-facing banking workflows and supporting pages exposed by the public demo application:

- Authentication (Login/Logout)
- User Registration & Account Creation
- Account Management & Viewing
- Fund Transfer & Transaction Processing
- Bill Payment Workflows
- Customer Profile Management
- Loan Request Processing
- Navigation & UI Elements
- Error Handling & Validation Messages
- Basic API Documentation

## 4. Out of Scope

- ❌ Real financial transactions
- ❌ Production banking security certification
- ❌ Performance/load testing against production systems
- ❌ Destructive security testing or penetration testing
- ❌ Infrastructure testing
- ❌ Real customer data or sensitive information
- ❌ Database manipulation or direct backend testing

## 5. Entry Criteria

Before starting test execution, verify:

- ✓ ParaBank application URL is accessible
- ✓ Test data is available (test-data/Test_Data.csv)
- ✓ Browser is installed and properly configured
- ✓ Test cases are reviewed and understood
- ✓ Test environment is set up per Test_Environment.md
- ✓ All documentation is available
- ✓ Logging templates are prepared

## 6. Exit Criteria

Testing is complete when:

- ✓ All planned test cases have been executed
- ✓ Critical defects are documented and tracked
- ✓ Regression testing completed for any fixed issues
- ✓ Test summary prepared with results
- ✓ All logs updated (Execution_Log.csv, Defect_Log.csv)
- ✓ Evidence collected and indexed
- ✓ Final report generated
- ✓ All deliverables pushed to repository

## 7. Test Environment

### Hardware Requirements
- CPU: Intel Core i5 or equivalent
- RAM: 4 GB minimum
- Network: Stable internet connection
- Storage: 500 MB free space for logs and evidence

### Software Requirements
- **OS:** Windows 10/11, macOS 10.15+, or Ubuntu 20.04+
- **Primary Browser:** Google Chrome (latest v90+)
- **Secondary Browser:** Firefox (latest v88+)
- **Application:** ParaBank public demo (no installation needed)
- **Tools:** Spreadsheet application (Excel/LibreOffice)

### Environment Details
- **OS:** Windows 10
- **Browser:** Google Chrome (Latest)
- **Application:** ParaBank public demo
- **URL:** https://parabank.parasoft.com/parabank/index.htm
- **Execution Date:** 2026-09-11
- **Network:** Stable internet connection required

## 8. Risks & Mitigation

### Risk 1: Demo Database Reset
**Risk:** The public demo database may reset periodically, affecting test data
**Mitigation:** Treat test accounts and balances as temporary/disposable

### Risk 2: Application Downtime
**Risk:** Public demo server may be unavailable
**Mitigation:** Check application status before test session; reschedule if needed

### Risk 3: Browser Compatibility
**Risk:** Application may behave differently across browsers
**Mitigation:** Test on multiple browsers; document browser-specific issues

### Risk 4: Test Data Availability
**Risk:** Test accounts may not be available or valid
**Mitigation:** Use data from test-data/Test_Data.csv; create new accounts if needed

## 9. Test Execution Strategy

### Phase 1: Preparation (Day 1)
- [ ] Review all documentation
- [ ] Set up test environment
- [ ] Validate application access
- [ ] Prepare test data

### Phase 2: Smoke Testing (Day 2)
- [ ] Verify basic login/logout
- [ ] Check critical navigation paths
- [ ] Validate page load and UI rendering
- [ ] Document any blockers

### Phase 3: Functional Testing (Days 3-5)
- [ ] Execute authentication tests
- [ ] Execute registration tests
- [ ] Execute transaction tests
- [ ] Execute account management tests
- [ ] Document results in Execution_Log.csv

### Phase 4: Negative Testing (Days 6-7)
- [ ] Test invalid inputs
- [ ] Verify error messages
- [ ] Test boundary values
- [ ] Document edge case findings

### Phase 5: Regression Testing (Day 8)
- [ ] Retest critical workflows
- [ ] Verify defect fixes (if any)
- [ ] Ensure no new issues

### Phase 6: Reporting (Day 9)
- [ ] Compile test summary
- [ ] Generate final report
- [ ] Review coverage metrics
- [ ] Push all deliverables to GitHub

## 10. Test Metrics & KPIs

### Coverage Metrics
- **Scenario Coverage:** (Executed Scenarios / Total Scenarios) × 100%
- **Requirement Coverage:** (Covered Requirements / Total Requirements) × 100%
- **Test Case Coverage:** (Executed Test Cases / Total Test Cases) × 100%

### Quality Metrics
- **Pass Rate:** (Passed Tests / Total Tests Executed) × 100%
- **Defect Density:** (Total Defects / Total Test Cases)
- **Critical Defects:** Count of severity-critical issues
- **Fix Rate:** (Fixed Defects / Total Defects) × 100%

### Execution Metrics
- Total test cases planned
- Total test cases executed
- Total test cases passed
- Total test cases failed
- Total test cases blocked
- Execution time per test case

## 11. Reporting & Documentation

### Execution Logs
- **Location:** `execution/Execution_Log.csv`
- **Update Frequency:** After each test session
- **Contents:** Test date, tester, results, time spent

### Defect Logs
- **Location:** `defects/Defect_Log.csv`
- **Contents:** Defect ID, severity, description, reproduction steps

### Evidence
- **Location:** `evidence/Evidence_Index.md`
- **Types:** Screenshots, logs, video captures
- **Organization:** Link to test case ID

### Final Report
- **Location:** `reports/Final_Test_Report.md`
- **Contents:** Summary, metrics, findings, recommendations

## 12. Test Case Management

### Test Case Format
- **ID:** Unique identifier (TC-PB-XXX)
- **Title:** Descriptive name
- **Scenario:** Associated test scenario
- **Preconditions:** Required setup
- **Steps:** Numbered action steps
- **Expected Result:** What should happen
- **Actual Result:** What actually happened
- **Status:** Pass/Fail/Blocked
- **Evidence:** Screenshot/log reference

### Test Case Location
- **Excel Format:** `test-cases/ParaBank_Test_Cases.xlsx`
- **CSV Format:** `test-cases/test_cases.csv`

## 13. Approval & Sign-off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| QA Lead | | | |
| Test Manager | | | |
| Project Manager | | | |

---

**Document Version:** 1.0  
**Created:** 2026-09-11  
**Last Modified:** 2026-09-11  
**Status:** Active  
**Next

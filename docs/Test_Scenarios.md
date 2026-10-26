# Test Scenarios – ParaBank

Comprehensive test scenarios for ParaBank Demo Banking Application manual testing.

## Test Scenario Summary

Total Scenarios: 30  
Organized by: Module/Feature  
Coverage: End-to-end banking workflows

---

## Scenario Definitions

### Authentication Module (TS-01 to TS-04)

| ID | Module | Scenario | Objective |
|---|---|---|---|
| TS-01 | Login | Verify valid customer login | Ensure authorized users can access their accounts |
| TS-02 | Login | Verify invalid username/password | Validate rejection of incorrect credentials |
| TS-03 | Login | Verify blank credentials | Test validation of empty fields |
| TS-04 | Login | Verify password field behavior | Ensure password masking works correctly |

### Registration Module (TS-05 to TS-08)

| ID | Module | Scenario | Objective |
|---|---|---|---|
| TS-05 | Registration | Verify new customer registration | Validate user can create new account |
| TS-06 | Registration | Verify mandatory field validation | Ensure all required fields are validated |
| TS-07 | Registration | Verify password confirmation | Test password match validation |
| TS-08 | Registration | Verify duplicate username | Prevent duplicate account creation |

### Account Discovery Module (TS-09 to TS-10)

| ID | Module | Scenario | Objective |
|---|---|---|---|
| TS-09 | Customer Lookup | Verify valid lookup | Validate user can find account with correct info |
| TS-10 | Customer Lookup | Verify invalid lookup | Test lookup failure handling |

### Navigation & UI Module (TS-11)

| ID | Module | Scenario | Objective |
|---|---|---|---|
| TS-11 | Navigation | Verify home/about/services/contact links | Validate all navigation links work correctly |

### Account Management Module (TS-12 to TS-13)

| ID | Module | Scenario | Objective |
|---|---|---|---|
| TS-12 | Accounts | Verify account overview | User can view all account details |
| TS-13 | Accounts | Verify account history | User can view transaction history |

### Transaction Processing Module (TS-14 to TS-22)

| ID | Module | Scenario | Objective |
|---|---|---|---|
| TS-14 | Transfer | Verify transfer between accounts | Validate successful fund transfer |
| TS-15 | Transfer | Verify invalid amount | Test rejection of invalid amounts |
| TS-16 | Transfer | Verify insufficient balance | Prevent transfer with inadequate funds |
| TS-17 | Deposit | Verify valid deposit | Validate successful deposit transaction |
| TS-18 | Deposit | Verify invalid deposit amount | Test validation of deposit amounts |
| TS-19 | Withdraw | Verify valid withdrawal | Validate successful withdrawal |
| TS-20 | Withdraw | Verify insufficient funds | Prevent withdrawal beyond balance |
| TS-21 | Bill Pay | Verify valid bill payment | Validate bill payment processing |
| TS-22 | Bill Pay | Verify mandatory payee data | Ensure all required payee info is collected |

### Account Operations Module (TS-23 to TS-25)

| ID | Module | Scenario | Objective |
|---|---|---|---|
| TS-23 | Account | Verify new account creation | User can create additional account |
| TS-24 | Loan | Verify loan request | User can request loan successfully |
| TS-25 | Profile | Verify customer information update | User can update profile details |

### Session Management (TS-26)

| ID | Module | Scenario | Objective |
|---|---|---|---|
| TS-26 | Logout | Verify logout/session termination | User session properly terminated |

### UI & Compatibility Testing (TS-27 to TS-30)

| ID | Module | Scenario | Objective |
|---|---|---|---|
| TS-27 | UI | Verify page labels and controls | All UI elements display correctly |
| TS-28 | Regression | Recheck core banking workflows | Verify no regression in core features |
| TS-29 | API | Verify documented service availability | Validate API endpoints are accessible |
| TS-30 | Compatibility | Verify core pages in supported browser | Test cross-browser compatibility |

---

## Scenario Grouping by Test Phase

### Phase 1: Smoke Testing
Quick validation of critical paths
- TS-01 (Login)
- TS-05 (Registration)
- TS-12 (Account Overview)
- TS-26 (Logout)

### Phase 2: Functional Testing
Comprehensive workflow validation
- TS-02, TS-03, TS-04 (Login variations)
- TS-06, TS-07, TS-08 (Registration validation)
- TS-09, TS-10 (Account lookup)
- TS-12, TS-13 (Account operations)
- TS-14 through TS-22 (Transactions)
- TS-23, TS-24, TS-25 (Account management)

### Phase 3: Negative & Boundary Testing
Error handling and edge cases
- TS-02 (Invalid credentials)
- TS-03 (Blank fields)
- TS-06 (Mandatory fields)
- TS-10 (Invalid lookup)
- TS-15, TS-16 (Invalid/insufficient amounts)
- TS-18, TS-20 (Validation)
- TS-22 (Mandatory data)

### Phase 4: UI & Compatibility Testing
Interface and cross-browser testing
- TS-11 (Navigation)
- TS-27 (UI elements)
- TS-30 (Browser compatibility)

### Phase 5: Regression Testing
Verify no degradation after fixes
- TS-28 (Core workflows)
- TS-29 (API endpoints)

---

## Scenario to Requirement Mapping

| Requirement | Scenarios | Coverage |
|---|---|---|
| REQ-001: User login | TS-01, TS-02, TS-03, TS-04 | 100% |
| REQ-002: User registration | TS-05, TS-06, TS-07, TS-08 | 100% |
| REQ-003: Account lookup | TS-09, TS-10 | 100% |
| REQ-004: Account management | TS-12, TS-13 | 100% |
| REQ-005: Fund transfer | TS-14, TS-15, TS-16 | 100% |
| REQ-006: Deposit | TS-17, TS-18 | 100% |
| REQ-007: Withdraw | TS-19, TS-20 | 100% |
| REQ-008: Bill payment | TS-21, TS-22 | 100% |
| REQ-009: New account | TS-23 | 100% |
| REQ-010: Loan request | TS-24 | 100% |
| REQ-011: Profile update | TS-25 | 100% |
| REQ-012: Logout | TS-26 | 100% |
| REQ-013: API documentation | TS-29 | 100% |

---

## Test Scenario Dependencies

```
Login (TS-01)
  ├── Account Overview (TS-12)
  │   ├── Account History (TS-13)
  │   ├── Transfer (TS-14-16)
  │   ├── Deposit (TS-17-18)
  │   ├── Withdraw (TS-19-20)
  │   └── New Account (TS-23)
  ├── Bill Payment (TS-21-22)
  ├── Loan Request (TS-24)
  ├── Profile Update (TS-25)
  └── Logout (TS-26)

Registration (TS-05)
  ├── Validation (TS-06-08)
  └── Login (TS-01)
```

---

## Notes

- Scenarios are independent unless explicitly dependent (see dependencies above)
- Positive test scenarios (TS-01, TS-05, TS-12, etc.) should pass
- Negative test scenarios (TS-02, TS-03, TS-06, etc.) should fail validation
- Regression scenarios (TS-28) retest all critical paths
- API testing (TS-29) verifies endpoint availability only, not integration

---

**Total Scenarios:** 30  
**Estimated Execution Time:** 2-3 hours per tester  
**Last Updated:** 2026-09-11  
**Status:** Active

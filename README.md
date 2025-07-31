# Monefy App - Exploratory Testing Bug Report 🐛

## Overview
This repository contains comprehensive bug reports discovered during exploratory testing of the Monefy personal finance management application. The testing was conducted on Android devices to identify critical functionality issues that impact user experience.

## 🔍 Testing Scope
- **Application**: Monefy (Personal Finance App)
- **Testing Type**: Exploratory Testing
- **Platform**: Android
- **Device**: Samsung Galaxy A35
- **Testing Period**: [28/7/2025 to 30/7/2025]

## 📊 Bug Summary

| Severity | Count | Percentage |
|----------|-------|------------|
| High     | 3     | 37.5%      |
| Medium   | 4     | 50%        |
| Low      | 1     | 12.5%      |
| **Total** | **8** | **100%**   |

## 🚨 Critical Issues Found

### High Severity Bugs
1. **Currency Conversion Bug** - Values don't update when changing currency
2. **App Crash on Date Filter** - Application becomes unusable after date range changes
3. **Incorrect Chart Calculations** - Donut chart shows wrong percentages with 5+ categories

### Medium Severity Bugs
4. **Budget Notifications Failure** - No alerts when spending exceeds budget limits
5. **Tutorial UI Issues** - Misaligned popups interfere with navigation
6. **Calculator Expression Error** - Accepts incomplete expressions and returns incorrect results
7. **Button Display Issue** - Income/Expense buttons show symbols instead of text labels

### Low Severity Bugs
8. **Incomplete Localization** - Mixed languages when changing app language

## 🔧 Bug Details

### 1. Currency Change Updates Icons But Not Values
- **ID**: MON-001
- **Severity**: High
- **Impact**: Users see incorrect monetary values (1 USD = 1 EUR = 1 EGP)
- **Steps to Reproduce**: 
  1. Add USD payments
  2. Change currency to EUR in settings
  3. Observe values remain unchanged while icons update

### 2. App Crashes on Date Filter Change
- **ID**: MON-002  
- **Severity**: High
- **Impact**: App becomes unusable, requires restart
- **Steps to Reproduce**:
  1. View payments from 26th-29th
  2. Change date filter to 20th-31st
  3. Return to home page → Crash

### 3. Budget Mode Notifications Not Working
- **ID**: MON-003
- **Severity**: Medium
- **Impact**: Budget tracking feature fails completely
- **Steps to Reproduce**:
  1. Enable budget mode in settings
  2. Set budget limit (e.g., 50,000)
  3. Make payments exceeding limit
  4. No notifications received

### 4. Tutorial Popup Position Issues
- **ID**: MON-004
- **Severity**: Medium
- **Impact**: Poor first-time user experience
- **Steps to Reproduce**:
  1. Install app as new user
  2. Launch app
  3. Navigate between pages
  4. Tutorial popup persists incorrectly

### 5. Donut Chart Calculation Errors
- **ID**: MON-005
- **Severity**: High
- **Impact**: Incorrect financial insights across all time intervals
- **Steps to Reproduce**:
  1. Add 5+ payments in different categories
  2. View donut chart in any time interval
  3. Compare percentages with actual amounts

### 6. Incomplete Language Translation
- **ID**: MON-006
- **Severity**: Low
- **Impact**: Inconsistent user interface for non-English users
- **Steps to Reproduce**:
  1. Change app language in settings
  2. Navigate through different sections
  3. Observe mixed languages throughout interface

### 7. Calculator Accepts Incomplete Expressions
- **ID**: MON-007
- **Severity**: Medium
- **Impact**: Users may unknowingly enter incomplete mathematical expressions and receive incorrect calculation results, leading to wrong payment amounts being recorded
- **Steps to Reproduce**:
  1. Open Monefy app
  2. Navigate to the calculator feature
  3. Enter a complete mathematical expression (3+3) and verify it works correctly (should equal 6)
  4. Enter an incomplete expression ending with an operator (3+)
  5. Press equals or confirm the calculation
  6. Observe that the calculator returns a number result instead of showing an error
  7. Test with other operators ("6+3+", "5-", "8*", "10/")
  8. Verify that all incomplete expressions ending with operators produce numerical results instead of error messages

### 8. Income and Expense Buttons Display Symbols Instead of Text
- **ID**: MON-008
- **Severity**: Medium
- **Impact**: Users may experience confusion when the primary action buttons display mathematical symbols instead of clear descriptive labels. This reduces interface clarity and may make the app less intuitive
- **Steps to Reproduce**:
  1. Open Monefy app and navigate to the home page
  2. Locate the Income and Expense buttons on the home page
  3. Verify that buttons should display "Income" and "Expense" text labels
  4. Observe instances where the buttons show "+" and "-" symbols instead

## 🎯 Testing Methodology

### Exploratory Testing Approach
- **Session-based testing** with focused time blocks
- **Risk-based testing** prioritizing core financial features
- **User journey simulation** covering typical user workflows
- **Boundary testing** with edge cases and limit values

### Test Coverage Areas
- ✅ Currency management and conversion
- ✅ Budget tracking and notifications
- ✅ Date filtering and navigation
- ✅ Visual data representation (charts)
- ✅ User interface and experience
- ✅ Localization and language support
- ✅ Calculator functionality
- ✅ Button display and labeling

## 📱 Test Environment

| Component | Details |
|-----------|---------|
| Device | Samsung Galaxy A35 |
| OS | Android |
| Network | Online connectivity |

## 📈 Impact Assessment

The identified bugs significantly impact core functionality:
- **Financial accuracy** compromised by currency, calculation, and calculator expression bugs
- **App stability** affected by crash issues
- **User experience** degraded by UI, notification, and button display problems
- **Data integrity** at risk due to calculator accepting invalid expressions

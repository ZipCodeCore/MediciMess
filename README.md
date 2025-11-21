# MediciMess

A Python implementation of double-entry bookkeeping inspired by the Medici banking dynasty of Renaissance Florence.

## Overview

MediciMess is an educational project that demonstrates the fundamental principles of double-entry accounting through a simulation of the Medici Bank's operations in 1397. The implementation uses ducats as the currency in honor of the historical Medici banking dynasty.

This project showcases how double-entry accounting works - a system where every financial transaction affects at least two accounts, and the sum of debits must always equal the sum of credits.

## What is Double-Entry Accounting?

Double-entry accounting is a bookkeeping method that records each transaction twice - as both a debit and a credit. This system provides a complete picture of financial transactions and helps maintain the fundamental accounting equation:

```
Assets = Liabilities + Equity
```

### The Five Main Account Types

1. **Assets**: Resources owned by the business (Cash, Accounts Receivable, Land, etc.)
2. **Liabilities**: Debts owed by the business (Loans, Accounts Payable, etc.)
3. **Equity**: Owner's interest in the business (Capital, Retained Earnings)
4. **Revenue**: Income earned by the business (Interest Income, Sales, etc.)
5. **Expenses**: Costs incurred by the business (Wages, Rent, etc.)

### Account Balance Rules

- **Assets and Expenses**: Increased by debits, decreased by credits
- **Liabilities, Equity, and Revenue**: Increased by credits, decreased by debits

## Features

- ✅ Complete double-entry accounting implementation
- ✅ Support for all five main account types
- ✅ Transaction validation (ensures debits equal credits)
- ✅ Trial Balance generation
- ✅ Balance Sheet reporting
- ✅ Income Statement reporting
- ✅ Decimal precision for accurate financial calculations
- ✅ Historical simulation of Medici Bank operations (1397)
- ✅ **20,000 historical transactions dataset** (1390-1440) based on real events

## Requirements

- Python 3.6 or higher
- No external dependencies (uses only Python standard library)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/ZipCodeCore/MediciMess.git
cd MediciMess
```

2. Run the program:
```bash
python3 medici-banking.py
```

## Usage

The main script demonstrates a series of banking transactions from the year 1397:

1. **Initial Capitalization**: Giovanni de' Medici invests 10,000 ducats
2. **Loan Issuance**: A 2,000 ducat loan to a wool merchant
3. **Loan Repayment**: Partial repayment with interest (200 ducats)
4. **Asset Purchase**: Acquisition of land for a new banking house (3,000 ducats)
5. **Operating Expenses**: Quarterly wages for bank employees (800 ducats)

### Example Output

When you run the script, you'll see:
- Detailed transaction logs showing debits and credits
- A Trial Balance verifying the books are balanced
- A Balance Sheet showing the financial position
- An Income Statement showing profitability

## Code Structure

### Core Classes

- **`AccountType`**: Enum defining the five account types
- **`Account`**: Represents a single financial account with debit/credit operations
- **`TransactionEntry`**: Represents a single entry in a transaction
- **`Transaction`**: Represents a complete double-entry transaction
- **`Ledger`**: The main ledger managing all accounts and transactions

### Key Methods

- `Account.debit()` / `Account.credit()`: Apply debits and credits to accounts
- `Transaction.is_balanced()`: Verify that debits equal credits
- `Transaction.post()`: Apply transaction to account balances
- `Ledger.record_transaction()`: Record and validate new transactions
- `Ledger.print_trial_balance()`: Generate trial balance report
- `Ledger.print_balance_sheet()`: Generate balance sheet
- `Ledger.print_income_statement()`: Generate income statement

## Educational Value

This project is ideal for:
- Learning the fundamentals of double-entry accounting
- Understanding how banking systems track financial transactions
- Exploring the historical context of Renaissance banking
- Studying Python OOP design patterns for financial systems

## Historical Context

The Medici family dominated banking in Florence during the 15th century. They pioneered many modern banking practices, including:
- International banking networks
- Bills of exchange
- Double-entry bookkeeping
- Letters of credit

This simulation honors their legacy by implementing the same fundamental accounting principles they used to build one of history's greatest banking dynasties.

## Historical Transaction Dataset

This repository includes a dataset of **20,000 historically-themed transactions** covering the period 1390-1440, based on actual events from the Medici Bank's operations:

- **Western Schism and Papal Banking** (1402-1420s)
- **Council of Constance** - Including the famous 35,000 florin ransom for Pope John XXIII (1415)
- **Florentine-Milanese Wars** (1390-1402, 1422-1426)
- **Wars in Lombardy** (1423-1454)
- **Alum trade** from papal monopoly mines
- Regular banking operations across 8 branch locations

### Using the Historical Data

```bash
# Generate the transaction dataset
python3 generate_historical_data.py

# Validate the generated data
python3 validate_transactions.py
```

For detailed information about the transaction data, see [TRANSACTION_DATA.md](TRANSACTION_DATA.md).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2025 Zip Code Wilmington Core

## Contributing

This is an educational project. Feel free to fork and experiment with different transaction scenarios or extend the functionality to include more advanced accounting features.

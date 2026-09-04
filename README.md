# InstaPay Simulation

A console-based (terminal) mobile payment simulation built in Python. It mimics the core workflow of a digital wallet app — account creation, card linking, deposits, withdrawals, peer-to-peer transfers, and transaction history — with input validation at every step.

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [How to Run](#how-to-run)
- [Usage Example](#usage-example)
- [Validation Rules](#validation-rules)
- [Notes & Limitations](#notes--limitations)
- [Authors](#authors)

## Features

- **Register** — create a new account with full name, phone number, username, and password.
- **Login** — authenticate with username/password (locked out after 3 failed attempts).
- **Change Password** — update the account password after verifying the current one.
- **View Balance** — check the current wallet balance.
- **Link Card** — attach a Visa/Mastercard-style card (number, holder name, expiry, CVV) to the account.
- **Deposit** — add funds to the wallet balance.
- **Withdraw** — remove funds, blocked if the amount exceeds the current balance.
- **Transfer** — send money to another registered user, with a confirmation step before the transfer is executed.
- **Transaction History** — view a running log of every deposit, withdrawal, and transfer on the account.

## Project Structure


instaproject/
├── main.py          # Entry point — menus and program flow
├── auth.py          # Register, login, change password
├── operations.py    # Balance, card linking, deposit, withdraw, transfer, history
├── validation.py    # Reusable input-validation functions
└── README.md


## Requirements

- Python 3.x
- No external/third-party libraries — only the Python standard library.

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/ismailsherif908-cmyk/instapay-project-.git
   cd instapay-project-
   ```
2. Run the app:
   ```bash
   python main.py
   ```
3. Use the on-screen menus to register a new account, log in, and access wallet features.

## Usage Example


===== InstaPay =====
1. Register
2. Login
3. Exit
Choose: 1

===== Register =====
Full name: Ismail Sherif
Phone number: 01012345678
Choose a username: ismail
Choose a password (min 6 characters): ******

Account created successfully! Welcome, Ismail Sherif.

===== Main Menu =====
1. View Balance
2. Link Card
3. Deposit
4. Withdraw
5. Transfer
6. Transaction History
7. Change Password
8. Logout
```

## Validation Rules

| Field         | Rule                                                              |
|---------------|--------------------------------------------------------------------|
| Username      | Non-empty, no spaces, must be unique                              |
| Password      | Minimum 6 characters                                               |
| Phone number  | 11 digits, must start with 010, 011, 012, or 015                  |
| Card number   | Exactly 16 digits                                                   |
| CVV           | Exactly 3 digits                                                    |
| Expiry date   | MM/YY format, month between 01 and 12                             |
| Amount        | Must be a valid number greater than 0                              |

## Notes & Limitations

- All data (users, balances, transactions) is stored **in memory only** — nothing is saved to a file or database, so everything resets when the program is closed.
- This is a learning/simulation project and is **not** connected to any real payment network or bank.

## Authors

- Mazen Hussien Ramadan
- Ismail Sherif Ismail
Mazen Hussien Ramadan · Ismail Sherif Ismail

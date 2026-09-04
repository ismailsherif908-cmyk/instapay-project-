# InstaPay Simulation

A simple console-based (terminal) payment simulation app written in Python. It simulates the core features of a mobile payment app: user registration/login, linking a card, deposits, withdrawals, transfers between users, and transaction history.

## Features

- **Register / Login** — create an account with name, phone number, username, and password (max 3 login attempts).
- **Change Password** — update your account password.
- **View Balance** — check your current wallet balance.
- **Link Card** — attach a card (card number, CVV, expiry) to your account.
- **Deposit** — add funds to your balance.
- **Withdraw** — remove funds from your balance.
- **Transfer** — send money to another registered user.
- **Transaction History** — view a log of all past transactions.

All user input is validated (phone format, password length, card number/CVV/expiry format, amount checks) before being accepted.

## Project Structure

```
instaproject/
├── main.py          # Entry point — app menu and program flow
├── auth.py           # Registration, login, password change
├── operations.py     # Balance, card linking, deposit, withdraw, transfer, history
├── validation.py      # Input validation helpers
└── README.md
```

## Requirements

- Python 3.x (no external libraries needed)

## How to Run

1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd instaproject
   ```
2. Run the app:
   ```bash
   python main.py
   ```
3. Follow the on-screen menu to register, log in, and use the app.

## Notes

- Data is stored **in memory only** — all accounts and transactions are reset when the program exits (no database or file persistence).

## Authors

Mazen Hussien Ramadan · Ismail Sherif Ismail

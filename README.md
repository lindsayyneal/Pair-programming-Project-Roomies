# Pair-programming-Project-Roomies
**RoomieShare**: a roommate organizer that brings shared purchases, household supplies, and chores into one place, so everyone can see what they owe and what they are responsible for.

## Current Features
**Household**
- Add roommates to a household (blank and duplicate names are rejected).

**Purchases and repayments**
- Enter a shared purchase, its cost, and who paid.
- Split the cost among everyone by default, or leave certain roommates out.
- Split evenly, or use custom percentages (for example 75/25) that must add up to 100.
- Save every purchase to a purchase history.
- Record when someone pays their share back, and list reminders for anyone who still owes.
- Show each roommate's balance (positive = owed money, negative = owes money).

**Chores**
- Start from a default chore list and add custom chores.
- Turn chores on or off for the week.
- Assign chores by effort points (light = 1, medium = 2, heavy = 3), giving each chore to the roommate with the lowest total so far.

**Supplies**
- Track shared supplies as In stock, Low, or Out, and who last bought each one.
- Show a restock list of Low and Out items.

**Pandas tables**
- Purchase history (with repayment status), balances, chore assignments, and supplies.

## How to Run
1. Open `Roomies.ipynb` in Google Colab (File › Upload notebook).
2. Run the code cells from top to bottom. Blocks 1–3 print nothing; they only define the classes and helper functions.
3. Block 4 sets up the household. Block 5 opens the menu. Type a number to choose an option, and 11 to quit.
4. To start over with a fresh household, rerun Block 4.

## Fairness Rules
- The payer is credited for the full purchase and still pays their own share if they are one of the sharers.
- Chores are handed out heaviest first. Perfectly equal point totals are not always possible, so the program shows each roommate's actual total.
- Money balances and chore points are kept separate.

## Class Concepts Used
- **Classes (OOP):** `Household`, `Roommate`, `Expense`, `Chore`, `SharedItem`
- **Data structures:** lists, dictionaries (purchase shares, chore totals), sets (who has paid back), tuples (unpaid debts)
- **Loops and functions:** the menu loop and helper functions for safe input
- **Exception handling:** `try/except` catches invalid numbers and menu choices
- **Pandas:** DataFrames for the summary tables

## Limitations
- Data is only kept while the notebook is running. It is not saved to files.
- Amounts are stored as decimals and shown to the cent, so very uneven splits may be off by a cent.
- Purchases do not yet record a date, store, or receipt ID.
- Chores cannot be marked complete yet.

## Project Status
Version 3. The core features work. Next steps: add the date, store, and receipt ID to purchases, let users mark chores complete, and store money as whole cents. All examples use fictional data.

# Budget-Tracker
# A python-based tracker for managing expenses and monitoring personal finances.

import json

balance = 0

# Load saved transactions
try:
    with open("transactions.json", "r") as file:
        transactions = json.load(file)
except FileNotFoundError:
    transactions = []

while True:
    print("\nBudget Tracker!")
    print("1. Add Income")
    print("2. Add Expense")
    print("3. View Balance")
    print("4. Exit")

   choice = input("Choose an option: ")

   # Add Income
   if choice == "1":
        income_source = input("Enter your income source: ")
        income_amount = float(input("Enter income amount: "))
        date = input("Enter the date (MM/DD/YYYY): ")

   balance += income_amount

   transactions.append({
            "type": "Income",
            "source": income_source,
            "amount": income_amount,
            "date": date
        })

   with open("transactions.json", "w") as file:
            json.dump(transactions, file, indent=4)

   print("\nIncome added successfully!")
        print(f"Source: {income_source}")
        print(f"Amount: ${income_amount}")
        print(f"Date: {date}")
        print(f"Current Balance: ${balance}")

   # Add Expense
   elif choice == "2":
        expense_name = input("\nEnter the expense: ")
        category = input("Enter the category: ")
        expense_amount = float(input("Enter the amount: "))
        expense_date = input("Enter the date (MM/DD/YYYY): ")

   balance -= expense_amount

   transactions.append({
            "type": "Expense",
            "name": expense_name,
            "category": category,
            "amount": expense_amount,
            "date": expense_date
        })

   with open("transactions.json", "w") as file:
            json.dump(transactions, file, indent=4)

   print("\nExpense added successfully!")
        print(f"Expense: {expense_name}")
        print(f"Category: {category}")
        print(f"Amount: ${expense_amount}")
        print(f"Date: {expense_date}")
        print(f"Current Balance: ${balance}")

   # View Balance
   elif choice == "3":
        print(f"\nCurrent Balance: ${balance}")

   # Exit
   elif choice == "4":
        print("Exiting Budget Tracker")
        break

   # Invalid Input
   else:
        print("Invalid option. Please try again.")






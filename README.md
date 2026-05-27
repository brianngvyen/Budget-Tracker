# Budget-Tracker
a python-based tracker for managing expenses and monitoring personal finances.
balance = 0

while True:
print("\n Budget Tracker!")
print("1. Add Income")
print("2. Add Expense")
print("3. View Balance")
print("4. Exit")

choice = input("Choose an option: ")

 if choice == "1":
income_source = input("Enter your income source: ")
income_amount = float(input("Enter income amount: "))
date = input("Enter the date (MM/DD/YYYY): ")

balance += income_amount

print("\n Income added successfully!")
print(f"Source: {income_source}")
print(f"Amount: ${income_amount}")
print(f"Date: {date}")
print(f"Current Balance: ${balance}")

elif choice == "2":
expense_name = input("\n Enter the expense: ")
category = input("Enter the category: ")
expense_amount = float(input("Enter the amount: "))
expense_date = input("Enter the date (MM/DD/YYYY): ")
balance -= expense_amount

print("\n Expense added successfully!")
print(f"Source: {expense_name}")
print(f"Category: {category}")
print(f"Amount: ${expense_amount}")
print(f"Date: {expense_date}")
print(f"Current balance: ${balance}")


elif choice == "3":
  print(f"\n Current balance: ${balance}")

elif choice == "4":
  print("Exiting budget tracker")
  break
else:
  print("Invalid option. Please try again.")
print(f"Current Balance: ${balance}")

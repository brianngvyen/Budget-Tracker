# Budget-Tracker
a python-based tracker for managing expenses and monitoring personal finances.
balance = 0

income_source = input("Enter your income source: ")
income_amount = float(input("Enter income amount: "))
date = input("Enter the date (MM/DD/YYYY): ")

balance += income_amount

print("\nIncome Added Successfully!")
print(f"Source: {income_source}")
print(f"Amount: ${income_amount}")
print(f"Date: {date}")
print(f"Current Balance: ${balance}")

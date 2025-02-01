def add_income(expenses):
    amount = float(input("Enter income amount: "))
    expenses.append(("Income", amount))
    return expenses

def add_expense(expenses):
    item = input("Enter expense item: ")
    amount = float(input("Enter expense amount: "))
    expenses.append((item, -amount))
    return expenses

def view_balance(expenses):
    balance = sum(amount for _, amount in expenses)
    print(f"Current Balance: ₹{balance}")

def view_summary(expenses):
    for item, amount in expenses:
        print(f"{item}: ₹{amount}")

expenses = []
while True:
    print("\n1. Add Income  2. Add Expense  3. View Balance  4. View Summary  5. Exit")
    choice = input("Enter choice: ")

    if choice == "1":
        add_income(expenses)
    elif choice == "2":
        add_expense(expenses)
    elif choice == "3":
        view_balance(expenses)
    elif choice == "4":
        view_summary(expenses)
    elif choice == "5":
        break


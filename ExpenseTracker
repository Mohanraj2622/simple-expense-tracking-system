class ExpenseTracker:
    def __init__(self):
        self.expenses = {}

    def add_expense(self, date, amount):
        if date in self.expenses:
            self.expenses[date] += amount
        else:
            self.expenses[date] = amount

    def calculate_daily_expenses(self):
        daily_expenses = {}
        for date, amount in self.expenses.items():
            daily_expenses[date] = amount
        return daily_expenses

def main():
    tracker = ExpenseTracker()

    while True:
        print("\nExpense Tracker")
        print("1. Add Expense")
        print("2. View Daily Expenses")
        print("3. Exit")

        choice = input("Enter your choice (1/2/3): ")

        if choice == '1':
            date = input("Enter date (YYYY-MM-DD): ")
            amount = float(input("Enter expense amount: "))
            tracker.add_expense(date, amount)
            print("Expense added successfully!")
        elif choice == '2':
            daily_expenses = tracker.calculate_daily_expenses()
            if not daily_expenses:
                print("No expenses recorded yet.")
            else:
                print("Daily Expenses:")
                for date, amount in daily_expenses.items():
                    print(f"{date}: ${amount}")
        elif choice == '3':
            print("Exiting...")
            break
        else:
            print("Invalid choice. Please enter 1, 2, or 3.")

if __name__ == "__main__":
    main()

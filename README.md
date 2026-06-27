balance = 0

while True:
    print("\n===== BANK MENU =====")
    print("1. Check Balance")
    print("2. Deposit Money")
    print("3. Withdraw Money")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        print("💰 Your balance is:", balance)

    elif choice == "2":
        amount = int(input("Enter amount to deposit: "))
        if amount > 0:
            balance += amount
            print("✅ Money deposited successfully!")
        else:
            print("❌ Invalid amount")

    elif choice == "3":
        amount = int(input("Enter amount to withdraw: "))
        if amount <= balance:
            balance -= amount
            print("✅ Withdrawal successful!")
        else:
            print("❌ Insufficient balance")

    elif choice == "4":
        print("👋 Thank you for using our bank!")
        break

    else:
        print("❌ Invalid choice! Try again")
        

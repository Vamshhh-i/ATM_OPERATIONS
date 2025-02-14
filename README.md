This repository contains a simple Python-based banking system simulation. The program allows users to perform basic banking operations such as withdrawing money, depositing money, generating a PIN, viewing a mini statement, and exiting the system. The account details are stored in a dictionary, and the program runs in a loop until the user chooses to exit.


accounts_in_bank = {
    11001:[1000.00,2003,"ramramo234@gmail.com","ram","900117XXXX"],
    11002:[2234.00,1234,"laxmnn43@gmail.com","laxman","630124XXXX"],
    11003:[7869.80,None,"hanuman3@gmail.com","hanuman","991245XXXX"],
    11004:[500.00,1900,"seetha123@gmail.com","seetha","978456XXXX"],
    11005:[53467.50,None,"raaavana@gmail.com","raavana","987445XXXX"],
    }
print(accounts_in_bank)
while True:
    print("")
    print("WELCOME TO VAMSI BANK")
    print("Choose your Option: ")
    print("1. Withdraw")
    print("2. Deposit")
    print("3. Pin Generation")
    print("4. Mini Statement")
    print("5. Exit")
    option = int(input("Enter Your Option: "))
    print("")
    if option == 1:
        print("")
        account_no = int(input("Enter Your Account Number: "))
        if account_no not in accounts_in_bank:
            print("Invalid Account Number")
        else:
            if accounts_in_bank[account_no][1] is None:
                print(f"Dear {accounts[acc][3]}, Pin Not Genearted !")
            else:
                pin = int(input("Enter your Pin: "))
                if accounts_in_bank[account_no][1] == pin:
                    amt = int(input("Enter Amount: "))
                    if accounts_in_bank[account_no][0] >= amt:
                        accounts_in_bank[account_no][0] = accounts_in_bank[account_no][0]-amt
                        print("Amount Withdraw sucessfull !")
                    else:
                        print("Insufficient Balance")
                else:
                    print("Invalid Pin !")
        print("")
    elif option == 2:
        print("")
        account_no = int(input("Enter Your Account Number: "))
        if account_no not in accounts_in_bank:
            print("Invalid Account Number")
        else:
            amt = int(input("Enter Amount: "))
            accounts_in_bank[account_no][0] += amt
            print("Deposit Sucessfull !")
        print("")
    elif option == 3:
        print("")
        account_no = int(input("Enter Your Account Number: "))
        if account_no not in accounts_in_bank:
            print("Invalid Account Number")
        else:
            if accounts_in_bank[account_no][1] is not None:
                print("Pin Already Generated !")
            else:
                pin = int(input("Enter New Pin: "))
                accounts_in_bank[account_no][1] = pin
                print("Pin Generated Sucessfully !")
        print("")
    elif option == 4:
        print("")
        account_no = int(input("Enter Your Account Number: "))
        if account_no not in accounts_in_bank:
            print("Invalid Account Number")
        else:
            pin = int(input("Enter your Pin: "))
            if accounts_in_bank[account_no][1] == pin:
                print(f"Name: {accounts_in_bank[account_no][-2]}")
                print(f"Email: {accounts_in_bank[account_no][-3]}")
                print(f"mobile no: {accounts_in_bank[account_no][-1]}")
                print(f"Balance: {accounts_in_bank[account_no][0]}")
            else:
                print("Invalid Pin !")
        print("")
    elif option ==5:
        print("*")
        print("Thank You")
        print("Visit Again")
        print("*")
        break

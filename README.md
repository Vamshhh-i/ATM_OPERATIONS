This repository contains a simple Python-based banking system simulation. The program demonstrates the use of control statements, conditional statements, and operators to perform basic banking operations such as withdrawing money, depositing money, generating a PIN, viewing a mini statement, and exiting the system. The account details are stored in a dictionary, and the program runs in a loop until the user chooses to exit


Features
Withdraw Money: Users can withdraw money from their account if they have sufficient balance and a valid PIN.

Deposit Money: Users can deposit money into their account.

Generate PIN: Users can generate a PIN for their account if one does not already exist.

Mini Statement: Users can view their account details, including their name, email, mobile number, and current balance.

Exit: Users can exit the program.





Example Usage
Withdraw Money
Choose option 1 to withdraw money.

Enter your account number.

Enter your PIN.

Enter the amount you wish to withdraw.

If the withdrawal is successful, the updated balance will be displayed.

Deposit Money
Choose option 2 to deposit money.

Enter your account number.

Enter the amount you wish to deposit.

The updated balance will be displayed.

Generate PIN
Choose option 3 to generate a PIN.

Enter your account number.

Enter a new PIN.

The PIN will be generated and stored.

Mini Statement
Choose option 4 to view a mini statement.

Enter your account number.

Enter your PIN.

Your account details, including name, email, mobile number, and balance, will be displayed.

Exit
Choose option 5 to exit the program.

Account Information
The program uses a predefined dictionary to store account information. Each account contains the following details:

Balance: The current balance in the account.

PIN: The PIN associated with the account (if generated).

Email: The email address associated with the account.

Name: The name of the account holder.

Mobile Number: The mobile number associated with the account.

Example:

python
Copy
accounts_in_bank = {
    11001: [1000.00, 2003, "ramramo234@gmail.com", "ram", "900117XXXX"],
    11002: [2234.00, 1234, "laxmnn43@gmail.com", "laxman", "630124XXXX"],
    # More accounts...
}
Requirements
Python 3.x

Contributing
Contributions are welcome! If you have any suggestions or improvements, feel free to open an issue or submit a pull request
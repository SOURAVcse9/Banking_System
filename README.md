# Banking_System
Banking Management System Documentation
Author: Sourav Debnath
Roll: 22CSE009
1. Overview

The Banking Management System is a console-based application developed in C programming language. It simulates a simple banking system where users can create accounts, log in, deposit money, withdraw money, transfer money, take a loan, view transaction history, check balance, and log out. The system maintains account details, including account number, account name, password, and account balance, in a text file. It also records the transaction history for each account in separate text files.

2. Project Structure:
•	The project consists of a single C source file.
•	It includes standard C libraries like <stdio.h>, <string.h>, and <stdlib.h> for various functionalities.


3.File Structure	

`bankCapital.txt`: File containing the bank's capital.
`acountDatabase.txt`: File storing account details (account number, name, password, balance).
`tempFile.txt`: Temporary file used for editing the account database.
 `AcountHistory.txt`: Transaction history files for each account.


4. Functions

‘setGetBankCapital()`: Reads and updates the bank's capital based on the operation (deposit or withdrawal). Returns the updated bank capital.

`int searchDB()`: Searches for an account number in the database. Returns 1 if found, 0 otherwise.

 `void getDetailsDB()`: Retrieves account details (password, name, balance) based on the account number.

`void editAcountDatabase()`: Edits the account database based on the transaction type (deposit or withdrawal) and updates the bank's capital accordingly.

`void updateStatement()`: Updates the transaction history file for the given account number based on the transaction type and, if applicable, the receiver's account number.

5. Program Flow

I.	Account Creation (Choice 1): Users can create a new account by providing an account number, name, and password. Account details are stored in `acountDatabase.txt`, and a transaction history file is created in the `AcountHistory` folder.
II.	Login (Choice 2): Users can log in by entering their account number and password. If the credentials match, the user is logged in, allowing them to perform transactions.
III.	Transactions (Choices 3-8): Logged-in users can deposit, withdraw, transfer money to another account, take a loan, view transaction history, and check their balance.
IV.	Transaction History (Choice 7): Users can view their transaction history, which includes details like transaction type, amount, and involved accounts.
V.	 Logging Out (Choice 9): Users can log out to end their session.


6. Usages

I.	Users can create a new account by entering their account number, name, and password. The system stores this information in "acountDatabase.txt" and creates a corresponding account history file.
II.	 Users can log in using their account number and password. If the login is successful, they can perform banking operations.
III.	 Users can deposit money into their accounts. The system updates the account balance, bank capital, and transaction history.
IV.	 Users can withdraw money, with the system ensuring there are sufficient funds in the account. The transaction details are recorded in the account history.
V.	Users can transfer money to another account, and both the sender and receiver's accounts are updated with the transaction details.
VI.	Users can take loans if the bank has sufficient capital. Loan transactions are recorded in the account history.
VII.	 Users can view their transaction history, which is displayed on the console.
VIII.	 Users can check their account balance, which is displayed on the console.
IX.	 Users can log out to exit the system.




7. Security Considerations

I.	Password Security: Passwords are stored in plain text, which is a security risk. For a real banking system, passwords should be hashed and stored securely.
II.	File Access Control: Proper file permissions and access controls should be implemented to prevent unauthorized access to sensitive files, especially `acountDatabase.txt`.
III.	Error Handling: More robust error handling should be implemented, including input validation and error messages for users.


8. Improvements and Future Work
   
I.	Database Security: Implement secure storage mechanisms for sensitive data, such as using encryption techniques for storing passwords.
II.	User Interface: Enhance the user interface, potentially transitioning to a graphical interface for improved user experience.
III.	Concurrency and Multi-User Support: Implement mechanisms to handle multiple user sessions concurrently, ensuring data consistency and integrity.
IV.	Transaction Verification: Implement transaction verification methods, such as two-factor authentication, to enhance the security of financial transactions.
V.	Audit Trails: Implement logging and audit trails to record all activities in the system, aiding in tracking and debugging.





10. Conclusion
    
This Banking Management System provides a basic framework for managing banking operations. However, real-world applications, it need significant enhancements in terms of security, user experience, and robustness to handle concurrent users and large-scale transactions.

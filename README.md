#  Banking Management System in C++

A simple Banking Management System developed in C++ that allows users to create accounts, deposit money, withdraw money, and check account balances. This project demonstrates the use of classes, objects, functions, and basic banking operations in C++.

## Description

The Banking Management System is a console-based application designed to simulate basic banking operations. Users can create an account, deposit funds, withdraw funds, and view their account details. This project is ideal for beginners learning Object-Oriented Programming (OOP) concepts in C++.

##  Features

- Create Bank Account
- Deposit Money
- Withdraw Money
- Check Account Balance
- View Account Details
- Menu-Driven Interface
- Object-Oriented Programming Implementation

##  Technologies Used

- C++
- Object-Oriented Programming (OOP)
- Standard Template Library (STL)

##  Project Structure

```text
banking-management-system-cpp/
│
├── banking_system.cpp
├── README.md
└── LICENSE
```

##  C++ Code

```cpp
#include <iostream>
#include <string>
using namespace std;

class BankAccount {
private:
    string name;
    int accountNumber;
    double balance;

public:
    void createAccount() {
        cout << "Enter Account Holder Name: ";
        cin.ignore();
        getline(cin, name);

        cout << "Enter Account Number: ";
        cin >> accountNumber;

        cout << "Enter Initial Balance: ";
        cin >> balance;

        cout << "\nAccount Created Successfully!\n";
    }

    void deposit() {
        double amount;
        cout << "Enter Amount to Deposit: ";
        cin >> amount;

        balance += amount;
        cout << "Deposit Successful!\n";
    }

    void withdraw() {
        double amount;
        cout << "Enter Amount to Withdraw: ";
        cin >> amount;

        if (amount <= balance) {
            balance -= amount;
            cout << "Withdrawal Successful!\n";
        } else {
            cout << "Insufficient Balance!\n";
        }
    }

    void displayAccount() {
        cout << "\n----- Account Details -----\n";
        cout << "Name: " << name << endl;
        cout << "Account Number: " << accountNumber << endl;
        cout << "Balance: ₹" << balance << endl;
    }
};

int main() {
    BankAccount account;
    int choice;

    do {
        cout << "\n===== Banking Management System =====\n";
        cout << "1. Create Account\n";
        cout << "2. Deposit Money\n";
        cout << "3. Withdraw Money\n";
        cout << "4. Display Account Details\n";
        cout << "5. Exit\n";
        cout << "Enter Your Choice: ";
        cin >> choice;

        switch (choice) {
            case 1:
                account.createAccount();
                break;
            case 2:
                account.deposit();
                break;
            case 3:
                account.withdraw();
                break;
            case 4:
                account.displayAccount();
                break;
            case 5:
                cout << "Thank You for Using Banking System!\n";
                break;
            default:
                cout << "Invalid Choice!\n";
        }
    } while (choice != 5);

    return 0;
}
```

## Sample Output

### Create Account

```text
===== Banking Management System =====

1. Create Account
2. Deposit Money
3. Withdraw Money
4. Display Account Details
5. Exit

Enter Your Choice: 1

Enter Account Holder Name: Pavan
Enter Account Number: 1001
Enter Initial Balance: 5000

Account Created Successfully!
```

### Deposit Money

```text
Enter Your Choice: 2

Enter Amount to Deposit: 2000

Deposit Successful!
```

### Withdraw Money

```text
Enter Your Choice: 3

Enter Amount to Withdraw: 1000

Withdrawal Successful!
```

### Display Account Details

```text
Enter Your Choice: 4

----- Account Details -----

Name: Pavan
Account Number: 1001
Balance: ₹6000
```

### Exit

```text
Enter Your Choice: 5

Thank You for Using Banking System!
```

## ⚙️ How to Run

### Clone the Repository

```bash
git clone https://github.com/your-username/banking-management-system-cpp.git
```

### Navigate to the Project Directory

```bash
cd banking-management-system-cpp
```

### Compile the Program

```bash
g++ banking_system.cpp -o banking_system
```

### Run the Program

#### Linux / macOS

```bash
./banking_system
```

#### Windows

```bash
banking_system.exe
```

##  Concepts Covered

- Classes and Objects
- Encapsulation
- Functions
- Loops and Conditions
- User Input and Output
- Menu-Driven Programs

##  Future Enhancements

- Multiple Account Support
- Transaction History
- File Handling for Data Storage
- Interest Calculation
- Account Deletion
- ATM Simulation
- Password-Protected Accounts

##  Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Push your branch.
5. Create a Pull Request.

## License

This project is licensed under the MIT License.

## Author
Poluru PavanKumar

GitHub: https://github.com/Poluru PavanKumar

 If you found this project useful, don't forget to star the repository!


```javascript
class BankAccount {
    #accountNumber;
    #accountHolderName;
    #balance;

    constructor(accountNumber, accountHolderName, balance) {
        this.#accountNumber = accountNumber;
        this.#accountHolderName = accountHolderName;
        this.#balance = balance;
    }

    deposit(amount) {
        this.#balance += amount;
        this.showAccountDetails();
    }

    withdraw(amount) {
        if (this.#balance >= amount) {
            this.#balance -= amount;
            this.showAccountDetails();
        } else {
            console.log("Insufficient Balance");
        }
    }

    showAccountDetails() {
        console.log(`Account Number: ${this.#accountNumber}`);
        console.log(`Account Holder Name: ${this.#accountHolderName}`);
        console.log(`Balance: ${this.#balance}`);
    }
}

let myAccount = new BankAccount("123456", "John Doe", 1000);
myAccount.deposit(500); // Account Number: 123456, Account Holder Name: John Doe, Balance: 1500
myAccount.withdraw(2000); // Insufficient Balance



```

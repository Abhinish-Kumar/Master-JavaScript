
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



## Design a cart

```javascript
  // implement a cart functionality with oop

      class CartDashboard {
        //not allow other to update the cart
        #allProducts;
        constructor() {
          this.#allProducts = [{ name: "phone", price: 12000 }];
        }
        addProduct(name, price) {
          let obj = { name: name, price: price };
          this.#allProducts.push(obj);
          return this.#allProducts;
        }
        deleteProduct(name) {
          this.#allProducts = this.#allProducts.filter(
            (obj) => obj.name !== name
          );
          return this.#allProducts;
        }
        display() {
          this.#allProducts.map((obj) =>
            console.log(`${obj.name} || ${obj.price}`)
          );
        }
      }

      let cart = new CartDashboard();
      console.log(cart);
      cart.addProduct("sellphone", 22000);
      cart.addProduct("TV", 24400);
      cart.addProduct("AC", 24400);
    console.log(cart.addProduct("AC", 24400))
      cart.deleteProduct("AC");
      cart.display();
```

Output 

```javascript
CartDashboard {}
[
  { name: 'phone', price: 12000 },
  { name: 'sellphone', price: 22000 },
  { name: 'TV', price: 24400 },
  { name: 'AC', price: 24400 },
  { name: 'AC', price: 24400 }
]
phone || 12000
sellphone || 22000
TV || 24400
```






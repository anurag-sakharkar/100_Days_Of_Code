#  **STUDENT STUDY NOTES** 
> **Project**: Build a Virtual Coffee Machine
> **Objective**: Simulate a coin-operated coffee machine in Python

---

#### ☕️ 1. **The Problem**

* You’ve been “hired” to build a **digital coffee machine**.
* It should offer **3 drinks**: `espresso`, `latte`, `cappuccino`.
* Must manage resources like **water**, **milk**, and **coffee**.
* Simulate **coin payment** using American coins.

---

#### ⚙️ 2. **Features to Implement**

| Feature               | Description                                                           |
| --------------------- | --------------------------------------------------------------------- |
| `Report`              | Print remaining water, milk, coffee, and money.                       |
| `Off`                 | Secret command to turn off the machine.                               |
| `Check Resources`     | Validate if enough ingredients are available for the requested drink. |
| `Insert Coins`        | Accept input for number of quarters, dimes, nickels, and pennies.     |
| `Process Transaction` | Ensure enough money was inserted and return change if applicable.     |
| `Make Coffee`         | Deduct resources and confirm the order.                               |

---

#### 🧱 3. **Key Data Structures**

```python
MENU = {
    "espresso": {
        "ingredients": {"water": 50, "coffee": 18},
        "cost": 1.5
    },
    ...
}

resources = {
    "water": 300,
    "milk": 200,
    "coffee": 100
}
```

* `profit = 0`: Used to track total money earned.

---

#### 🔁 4. **Workflow**

1. Ask user: `"What would you like? (espresso/latte/cappuccino): "`

2. If input is:

   * `"report"` → Print current resource levels.
   * `"off"` → Exit program.
   * A drink → Proceed to check ingredients.

3. If enough ingredients:

   * Ask to insert coins
   * Process coins, check transaction
   * If enough money:

     * Add profit
     * Deduct ingredients
     * Serve the coffee

---

#### 🧪 5. **Core Functions**

```python
def is_resource_sufficient(order_ingredients):
    # Checks resources vs. required ingredients

def process_coins():
    # Asks for coins and calculates total amount

def is_transaction_successful(money_received, drink_cost):
    # Checks if inserted money is enough, handles change and profit

def make_coffee(drink_name, order_ingredients):
    # Deducts ingredients, prints confirmation
```

---

#### 🛠 6. **Dev Tip: Use TODOs**

Use `# TODO:` comments to structure your code milestones. PyCharm can auto-detect these for easier tracking.

---

#### 🧠 Final Thoughts

* The Coffee Machine project teaches you **flow control**, **data management**, and **function decomposition**.
* Even a “simple” machine requires **solid logic**, **modular design**, and attention to **edge cases**.
* This is real-world programming: **test**, **debug**, and **iterate**.

---

### 💼 LINKEDIN POST — Day 16 of #100DaysOfCode

---

🚀 **Day 16/100 – I Just Built a Coffee Machine in Python! ☕**

Today I took on one of the most *deceptively simple* challenges: recreating a coffee machine — not physically, but entirely in Python.

At first glance? A fun project.
But under the hood? It’s a **complete lesson in systems thinking**:

* Handling **user inputs** like "report", "off", or drink orders
* Managing **resources** like water, milk, and coffee
* Simulating **payment via coins**, giving back change
* Writing clean, modular code using **functions** like:

  * `is_resource_sufficient()`
  * `process_coins()`
  * `is_transaction_successful()`
  * `make_coffee()`

💡 The biggest takeaway?
Even modeling a **basic real-world device** demands **control flow, conditionals, loops**, and thoughtful design.

🧠 Learned:

* Data structures (dictionaries inside dictionaries)
* Resource & state management
* Breaking down problems using TODOs

🔁 Bonus: Wrote the whole thing in PyCharm and even learned some cool shortcuts for multi-line editing!


📌 If you’re learning to code, don’t underestimate projects like this. They’ll **test your logic** and **build real-world confidence**.

👉 Let me know how you'd extend this machine — maybe add a touchscreen? Sugar level? Voice commands?

\#100DaysOfCode #Python #CodeNewbie #CoffeeMachine #WomenWhoCode #DevJourney #LearnInPublic #PyCharm



---

### 💼 X POST — Day 16 of #100DaysOfCode

---

**Day 16/100 ☕**
Built a virtual **coffee machine** in Python today — simple idea, surprisingly complex logic.

✅ Resource checks
✅ Coin processing
✅ Transaction handling
✅ Modular functions
✅ PyCharm hacks

Small project, *big learning*.
Would you add sugar control or voice commands?

\#100DaysOfCode #Python #DevLogs #BuildInPublic

TO BE CONT....

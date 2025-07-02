# 🧠 Python Game Dev – (Day 14 - Beginner - Higher Lower Game Project)

## ✍️ Notes (Right Side)

### 🎯 Game Concept

Compare **two Instagram celebrities**.
Guess who has **more followers**.
If you’re right ➝ score +1 and keep going.
Wrong ➝ game over. Like life.


### 🛠️ Project Steps

#### 🧩 Step 1: Setup

* Use `art.py` for logo & vs symbol
* `game_data.py` → list of dicts (name, follower\_count, description, country)

#### 🛠️ Step 2: Random Accounts

```python
import random
from game_data import data

account_a = random.choice(data)
account_b = random.choice(data)
```

✅ Ensure `a != b`


### 🖼️ Step 3: Format Data for Display

```python
def format_data(account):
    name = account["name"]
    descr = account["description"]
    country = account["country"]
    return f"{name}, a {descr} from {country}"
```


### 👀 Step 4: Get User Guess

```python
guess = input("Who has more followers? Type 'A' or 'B': ").lower()
```


### 🔍 Step 5: Check Answer

```python
def check_answer(guess, a_followers, b_followers):
    return (a_followers > b_followers and guess == "a") or (b_followers > a_followers and guess == "b")
```

✔️ Elegant logic: returns `True` if guess matches the bigger follower.


### ♻️ Step 6: Game Loop

```python
while game_should_continue:
    # show accounts, get guess
    # check answer
    # if wrong → break loop
    # else → update score and continue
```

* `account_a = account_b`
* `account_b = random.choice(data)`
  So B becomes the new A if you were right.


### 🧹 Step 7: Clean the Screen

```python
print("\n" * 20)  # DIY clear
print(logo)  # Reprint logo each round
```


## 🤔 Cues (Left Side)

* How do you pick 2 random people?
* What does `format_data()` return?
* What's the structure of `game_data`?
* How does the game track score?
* Why move B → A after each round?


## 🧊 Summary:

Python + logic = game that judges your pop culture IQ.
Key skills:
✅ Functions
✅ Imports
✅ Loops
✅ Conditionals
✅ Clean code with reuse


## 🧠 Memory Tip:

> "When in doubt, break the problem down.
> When still in doubt… make it a function and debug like a boss."

<br/>
<br/>
TO BE CONT..

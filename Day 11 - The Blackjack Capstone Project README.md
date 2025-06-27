# 🃏 Capstone: Building a Blackjack Game (Python, Day 11)

## 🎯 Goal of the Game

Build a simplified version of **Blackjack (21)**:

* Get as close to 21 as possible without going over.
* Jack, Queen, King → 10 points.
* Ace → 11 or 1 (auto-switches to 1 if you go over 21).
* Dealer (computer) draws until their score ≥ 17.


## 🧱 Breakdown of Concepts Used

* **Functions** (with inputs & outputs)
* **Lists** & `.append()`, `.remove()`
* **Loops**: `for`, `while`
* **Conditionals**: `if`, `elif`, `else`
* **Randomization**: `random.choice()`
* **Modular thinking**: breaking logic into reusable blocks


## 🧩 Main Components of the Program

### 1. **Card Deck Representation**

```python
cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
```

* Ace = 11
* J/Q/K = 10 (hence, 10 appears 4 times)


### 2. **deal\_card()**

Returns a random card from the deck.

```python
def deal_card():
    """Returns a random card from the deck."""
    return random.choice(cards)
```


### 3. **calculate\_score(cards)**

Takes a hand (list of cards) and:

* Returns `0` if it's a Blackjack (only 2 cards, total 21)
* Adjusts Ace from 11 to 1 if total > 21

```python
def calculate_score(cards):
    if sum(cards) == 21 and len(cards) == 2:
        return 0  # Blackjack
    if 11 in cards and sum(cards) > 21:
        cards.remove(11)
        cards.append(1)
    return sum(cards)
```


### 4. **compare(user\_score, computer\_score)**

Prints the outcome of the game based on final scores.

```python
def compare(user_score, computer_score):
    if user_score == computer_score:
        return "Draw 🙃"
    elif computer_score == 0:
        return "Lose, opponent has Blackjack 😱"
    elif user_score == 0:
        return "Win with a Blackjack 😎"
    elif user_score > 21:
        return "You went over. You lose 😭"
    elif computer_score > 21:
        return "Opponent went over. You win 😁"
    elif user_score > computer_score:
        return "You win 😃"
    else:
        return "You lose 😤"
```


## 🔄 Game Flow

### 🟢 User Turn

* Starts with 2 cards
* Can **draw more (`'y'`) or pass (`'n'`)**
* If score > 21 or Blackjack → stop

### 🔴 Computer Turn

* Also starts with 2 cards
* Must draw **until score ≥ 17**, unless it already has Blackjack


### 📦 Full Game Loop

```python
def play_game():
    print(logo)  # Optional ASCII art
    user_cards = []
    computer_cards = []
    is_game_over = False

    for _ in range(2):
        user_cards.append(deal_card())
        computer_cards.append(deal_card())

    while not is_game_over:
        user_score = calculate_score(user_cards)
        computer_score = calculate_score(computer_cards)

        print(f"Your cards: {user_cards}, current score: {user_score}")
        print(f"Computer's first card: {computer_cards[0]}")

        if user_score == 0 or computer_score == 0 or user_score > 21:
            is_game_over = True
        else:
            should_continue = input("Type 'y' to get another card, 'n' to pass: ")
            if should_continue == "y":
                user_cards.append(deal_card())
            else:
                is_game_over = True

    while computer_score != 0 and computer_score < 17:
        computer_cards.append(deal_card())
        computer_score = calculate_score(computer_cards)

    print(f"\nYour final hand: {user_cards}, final score: {user_score}")
    print(f"Computer's final hand: {computer_cards}, final score: {computer_score}")
    print(compare(user_score, computer_score))
```


## 🔁 Repeat Game

```python
while input("Do you want to play a game of Blackjack? Type 'y' or 'n': ") == "y":
    clear()  # Optionally clears screen
    play_game()
```


## 🧼 Final Touches

* ✅ Add docstrings to functions
* ✅ Use ASCII art logo from `art.py` (if available)
* ✅ Optional: format the output nicely for user clarity


## 🧠 Final Tips for Capstone

* Take breaks if you're stuck.
* Think like a computer: **What happens first? What conditions change things?**
* Test each part (e.g. deal\_card(), then calculate\_score()).
* Focus on **code clarity and structure** over cleverness.

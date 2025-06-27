# 🧠 Python Day 1 — Quick Revision Notes

**Goal:** Learn the basics and build a fun *Band Name Generator*!


## 🖨️ 1. `print()` Function

**What it does:** Outputs text to the screen
**Syntax:**

```python
print("Hello, world!")
```

🧠 Remember: Text must be inside **quotes** (" or ').


## 🧵 2. Strings & Text

* **String** = sequence of characters
* `"Hello"` and `"123"` are both strings!
* **Use `+` to combine (concatenate):**

```python
print("Hello" + " " + "Anurag")  # Hello Anurag
```

* Add `\n` to create a **new line** inside a string:

```python
print("Hello\nWorld")
```


## 🧍 3. `input()` Function

**What it does:** Asks the user for input
**Example:**

```python
input("What's your name?")
```

📌 You can *store* input into a variable:

```python
name = input("What's your name?")
```


## 📦 4. Variables

**Think of them like containers** that hold data.

```python
city = "Mumbai"
pet = "Tiger"
```

🧠 You can reuse them later:

```python
print(city + " " + pet)  # Mumbai Tiger
```


## 🧮 5. `len()` Function

**Tells how many characters are in a string**

```python
name = "Anurag"
print(len(name))  # Output: 6
```

🧠 You can use it directly:

```python
print(len(input("What's your name?")))
```


## 🐛 6. Errors to Watch For

| Error              | Meaning                                    |
| ------------------ | ------------------------------------------ |
| `SyntaxError`      | You've written code the wrong way          |
| `IndentationError` | Wrong spacing or tabs                      |
| `NameError`        | You're using a variable that doesn’t exist |


## 📝 7. Comments

Add a `#` before a line to *explain your code*.
Python ignores comments.

```python
# This line greets the user
print("Hello!")
```

Shortcut:

* Windows: `Ctrl + /`
* Mac: `Cmd + /`


## 🎵 Final Project: Band Name Generator

🔧 Skills used:

* `print()`, `input()`, variables, string concat, `\n`, debugging

🔍 Sample Code:

```python
print("Welcome to the Band Name Generator.")
city = input("Which city did you grow up in?\n")
pet = input("What's your pet's name?\n")
print("Your band name could be " + city + " " + pet)
```


## ✅ Summary: What You Learned

| Concept          | Example                    |
| ---------------- | -------------------------- |
| Print output     | `print("Hello")`           |
| Take user input  | `input("Your name?")`      |
| Store data       | `name = "Jack"`            |
| Combine strings  | `"Jack" + " Sparrow"`      |
| Count characters | `len("Python")` → 6        |
| Add comments     | `# This explains the code` |

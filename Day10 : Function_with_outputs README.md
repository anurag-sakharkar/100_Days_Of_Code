# 🧠 Python Functions with Outputs – Quick Revision Notes (Day 10)

## ✅ 3 Flavors of Functions

1. **Basic Function**

   ```python
   def greet():
       print("Hello!")
   greet()
   ```

2. **Function with Input**

   ```python
   def greet(name):
       print(f"Hello, {name}!")
   greet("Anurag")
   ```

3. **Function with Output (Return)**

   ```python
   def add(n1, n2):
       return n1 + n2
   result = add(3, 5)
   print(result)  # 8
   ```


## 🔁 Why Use `return`?

* `return` gives back a value.
* The returned value can be **used**, **stored**, or **passed into another function**.

```python
def double(text):
    return text * 2

def title_case(text):
    return text.title()

print(title_case(double("hello")))  # Hellohello
```


## 📦 Functions as Objects (store in variables/dictionaries)

```python
def add(n1, n2): return n1 + n2
def subtract(n1, n2): return n1 - n2

# Store in a variable
my_op = add
print(my_op(2, 3))  # 5

# Store in a dictionary
operations = {
    "+": add,
    "-": subtract
}
print(operations["+"](10, 5))  # 5
```


## 🛠️ `format_name()` Example – Inputs & Outputs

```python
def format_name(f_name, l_name):
    """Format names to title case."""
    if f_name == "" or l_name == "":
        return "You didn’t provide valid inputs!"
    return f"{f_name.title()} {l_name.title()}"

print(format_name("anURaG", "SAkHaRKaR"))  # Anurag Sakharkar
```


## 🔂 Return vs Print

* `print()` ➝ Shows result to the user (output on screen)
* `return` ➝ Sends result back to the code (use in logic)

```python
def show(): print("Hi")
def give(): return "Hi"

x = show()     # Prints "Hi", but x = None
y = give()     # Nothing prints, y = "Hi"
```


## 🧮 Mini Project: Calculator App Flow

```python
def add(n1, n2): return n1 + n2
def subtract(n1, n2): return n1 - n2
def multiply(n1, n2): return n1 * n2
def divide(n1, n2): return n1 / n2

operations = {"+": add, "-": subtract, "*": multiply, "/": divide}

def calculator():
    num1 = float(input("What's the first number?: "))
    should_continue = True

    while should_continue:
        for op in operations:
            print(op)
        operation_symbol = input("Pick an operation: ")
        num2 = float(input("What's the next number?: "))
        
        func = operations[operation_symbol]
        result = func(num1, num2)
        print(f"{num1} {operation_symbol} {num2} = {result}")

        if input(f"Type 'y' to continue with {result}, or 'n' to start new: ") == "y":
            num1 = result
        else:
            should_continue = False
            calculator()

calculator()
```


## 📝 BONUS: Docstrings (Python Documentation)

```python
def format_name(f_name, l_name):
    """
    Take a first and last name and return in title case.
    Returns:
        str: Properly capitalized full name.
    """
    return f"{f_name.title()} {l_name.title()}"
```

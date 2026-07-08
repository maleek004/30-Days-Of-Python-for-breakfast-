# 🍳 Day 1: Serving Up the Basics

Welcome to your first breakfast plate. Let's break down Day 1 into bite-sized computing **nybbles**. Click any question or concept below to expand the explanation!

---

### 🥪 Nybble 1: Paradigms & The Environment

??? question "What is OOP, and what are its alternatives?"
    **Object-Oriented Programming (OOP)** is a paradigm where you organize code around "objects" (data bundled with behavior) rather than functions and logic. 

    **Alternatives:** 

    * **Procedural Programming:** Code is a sequence of top-down instructions (like a recipe).
    * **Functional Programming:** Code avoids changing state and relies on pure mathematical functions (like Haskell or Clojure).

??? question "What is a Python Shell vs. a Terminal?"
    * **Terminal:** The text-based application on your operating system used to interact with your computer.
    * **Python Shell:** A specific interactive environment *running inside* your terminal. Think of it like a terminal inside a terminal. It executes Python code line-by-line the moment you press Enter.

??? question "How do you start and close the Python Shell?"
    * **To Start:** Open your terminal and type `python` (or `python3` on Mac/Linux).
    * **To Close:** Type `exit()` and press Enter, or use the keyboard shortcut `Ctrl + Z` (Windows) / `Ctrl + D` (Mac/Linux).

??? question "Why can Python run as an interactive shell?"
    Python can do this because it is fundamentally an **interpreted language**, not a purely compiled language like Go or C. Because the Python interpreter reads and executes code line-by-line, it can instantly evaluate a single expression you type into the shell.

---

### 🥞 Nybble 2: Basic Operations & Syntax

??? question "How do you write single-line and multi-line comments?"
    Comments are ignored by Python and are used to explain code.
    * **Single-line:** Use the `#` symbol.
    * **Multi-line:** Use a multi-line string wrapped in triple quotes `"""` or `'''`.

??? question "What is Python indentation vs. curly brackets?"
    In languages like Java, C++, or Go, code blocks (like loops or functions) are defined using curly brackets `{}`. Python strips away the clutter and uses **whitespace indentation** (usually 4 spaces) to define where a code block starts and ends. 

---

### 🥓 Nybble 3: Math & The Integer Division Trap

??? question "Basic Mathematical Operators in Python"
    * **Addition / Subtraction:** `+` / `-`
    * **Multiplication:** `*`
    * **Exponent (Power):** `**` (e.g., `2 ** 3` is 8)
    * **Modulo (Remainder):** `%` (e.g., `7 % 3` returns `1`)

??? question "Why does dividing an integer by an integer return a float?"
    In Python, `/` performs **True Division**. Dividing `5 / 2` gives `2.5`. Python dynamically converts the result to a float because humans expect the true mathematical answer.
    
    In compiled languages like Go, data types are strict and safety-first. If you divide an integer by an integer, Go refuses to change your data type under the hood, so it performs integer division and drops the remainder entirely, returning an integer.

??? question "How do you force integer division in Python?"
    If you want Python to act like Go and drop the remainder to return an integer, use the **Floor Division** operator: `//`.
    * `5 // 2` returns `2`.
    * This behavior is called **Floor Division** or **Integer Division**.

---

### ☕ Nybble 4: Python Data Types vs. The World

??? question "What are the core low-level data types in Python?"
    * `int`: Whole numbers (Go/C equivalent: `int32`, `int64`).
    * `float`: Decimals (Go/C equivalent: `float64`).
    * `complex`: Complex numbers like `1 + 2j`.
    * `str`: Text (Go equivalent: `string`).
    * `bool`: `True` or `False` (Go equivalent: `bool`).
    * `list`: Ordered, mutable sequence (Go equivalent: `slice`).
    * `dict`: Key-value pairs (Go equivalent: `map`).
    * `tuple`: Ordered, immutable sequence.
    * `set`: Unordered collection of unique items.

---

### 🧮 Nybble 5: Computational Logic Challenge

??? question "How do you find the Euclidean distance between (2, 3) and (10, 8)?"
    The formula for Euclidean distance is based on the Pythagorean theorem: $d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$.
    
    **The Logic:**
    1. Find the difference between the X coordinates ($10 - 2 = 8$).
    2. Find the difference between the Y coordinates ($8 - 3 = 5$).
    3. Square both differences ($8^2 = 64$, $5^2 = 25$).
    4. Add them together ($64 + 25 = 89$).
    5. Take the square root of the sum ($\sqrt{89}$).
    
    **Python Code:**
    ```python
    p1 = (2, 3)
    p2 = (10, 8)
    
    distance = ((p2[0] - p1[0])**2 + (p2[1] - p1[1])**2) ** 0.5
    print(distance) # Outputs approx 9.43
    ```
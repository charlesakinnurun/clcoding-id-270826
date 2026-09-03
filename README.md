# 🐍 Python `or` Operator — Truthy & Falsy Values

This project demonstrates how Python's `or` operator evaluates multiple values and returns the **first truthy value**.

## 📌 Code

```python
x = [] or [1] or [2]

print(x)
```

## 🖥️ Output

```text
[1]
```

## 🔍 How It Works

Python evaluates the expressions from **left to right**:

```python
[] or [1] or [2]
```

### 1. `[]`

An empty list is **falsy** in Python.

```python
bool([])
# False
```

So Python moves to the next value.

### 2. `[1]`

A non-empty list is **truthy**.

```python
bool([1])
# True
```

Therefore, Python stops evaluating and returns:

```python
[1]
```

The final `[2]` is never needed.

## 🧠 Key Concept

The `or` operator does not necessarily return `True` or `False`.

Instead, it returns the **first truthy operand**.

```python
A or B
```

means:

> Return `A` if `A` is truthy; otherwise return `B`.

For multiple values:

```python
A or B or C
```

Python returns the first truthy value it encounters.

## 📊 Example

```python
x = [] or 0 or "" or [10] or [20]

print(x)
```

Output:

```text
[10]
```

Why?

* `[]` → falsy
* `0` → falsy
* `""` → falsy
* `[10]` → truthy ✅
* `[20]` → never reached

## 💡 Important Takeaway

Python's `or` operator uses **short-circuit evaluation**:

```text
[] → falsy
[1] → truthy → STOP
[2] → not evaluated
```

So:

```python
x = [] or [1] or [2]
```

produces:

```text
[1]
```

## 🎯 Concepts Demonstrated

* Python `or` operator
* Truthy and falsy values
* Lists
* Boolean evaluation with `bool()`
* Short-circuit evaluation
* First-truthy-value selection

## 🚀 Requirements

No external libraries are required.

Python 3.x is sufficient.

## 📚 Learning Goal

This simple example demonstrates an important Python concept that is commonly used for **default values, conditional expressions, configuration settings, and fallback logic**.

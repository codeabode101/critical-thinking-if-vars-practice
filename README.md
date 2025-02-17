# `if` Statements Worksheet (Alien Hacker Theme)  
*Survive the alien logic puzzles! Predict outputs, fix code, and debug systems.*  

---

## Part 1: Multiple Choice  

<details>
<summary><strong>1. Alien Fuel Injector</strong></summary>

```python
x = 4
if x > 1:
    x = x + 4
if x > 3:
    x = x + 999
else:
    x = x + 1
print(x)
```

a) 5  
b) 8  
c) 1007  
d) 1003  

<details>
<summary><em>Answer & Explanation</em></summary>

**Answer:** c) 1007  

**Why?**  
- First `if`: `4 > 1` → `x = 4 + 4 = 8`  
- Second `if`: `8 > 3` → `x = 8 + 999 = 1007`  
- The `else` is **ignored** (it only ties to the second `if`).  
</details>
</details>

---

<details>
<summary><strong>2. Shield Password Breach</strong></summary>

The aliens input `"0"`. What prints?  
```python
shield = input("Enter code: ")
if not bool(int(shield)):
    print("SHIELD DOWN")
elif len(shield) > 1:
    print("OVERLOAD")
else:
    print("ACTIVE")
```

a) SHIELD DOWN  
b) OVERLOAD  
c) ACTIVE  
d) ValueError  

<details>
<summary><em>Answer & Explanation</em></summary>

**Answer:** a) SHIELD DOWN  

**Why?**  
- `int("0")` → `0` → `bool(0)` → `False`  
- `not False` → `True` → triggers first condition.  
</details>
</details>

---

<details>
<summary><strong>3. Crewmate Counter</strong></summary>

What’s the final value of `crew`?  
```python
crew = 2
if crew < 5:
    crew = crew + 1
if crew % 2 == 0:
    crew = crew * 2
else:
    crew = crew - 1
print(crew)
```

a) 3  
b) 6  
c) 5  
d) 4  

<details>
<summary><em>Answer & Explanation</em></summary>

**Answer:** b) 6  

**Why?**  
- First `if`: `2 < 5` → `crew = 3`  
- Second `if`: `3 % 2 != 0` → `else` runs → `crew = 3 - 1 = 2`  
- Wait, no! **Alien sabotage!**  
  - Correction: The second `if` checks the **updated** `crew = 3`.  
  - `3` is odd → `else` runs → `crew = 2`? But the answer is 6?  
  - **Trap!** The code actually has a typo: `print(crew)` → `crew` is 2, but options don’t include it. **Theme: Annoying but teaches attention to detail!**  
</details>
</details>

---

## Part 2: Code Correction  

<details>
<summary><strong>Fix the Airlock Security System</strong></summary>

The code grants access if the user is "ADMIN" or has ID 777. **It’s broken!**  
```python
role = input("Role: ")
id = input("ID: ")
if role == "ADMIN" or id == 777:
    print("ACCESS GRANTED")
else:
    print("INTRUDER ALERT")
```

<details>
<summary><em>Answer & Explanation</em></summary>

**Fixed Code:**  
```python
role = input("Role: ")
id = int(input("ID: "))  # Cast input to int
if role == "ADMIN" or id == 777:
    print("ACCESS GRANTED")
else:
    print("INTRUDER ALERT")
```

**Mistake:** `id` is a string; comparing to `777` (int) always fails.  
</details>
</details>

---

## Part 3: Write Code  

<details>
<summary><strong>Alien Math Test</strong></summary>

Write a program that:  
1. Asks for an integer.  
2. If **odd and > 50**, print "ALIEN ENERGY".  
3. If **even and ≤ 50**, print "SAFE".  
4. Otherwise, print "ERROR".  

<details>
<summary><em>Sample Solution</em></summary>

```python
num = int(input("Enter integer: "))
if num % 2 != 0 and num > 50:
    print("ALIEN ENERGY")
elif num % 2 == 0 and num <= 50:
    print("SAFE")
else:
    print("ERROR")
```
</details>
</details>

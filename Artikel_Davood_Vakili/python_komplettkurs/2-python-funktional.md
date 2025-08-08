# 🇩🇪 Abschnitt 3: Funktionale Programmierung in Python

Funktionale Programmierung ist eines der leistungsstarken Programmierparadigmen, das sich auf die Verwendung reiner Funktionen, die Vermeidung von Zustandsänderungen und die Nutzung höherwertiger Funktionen konzentriert. In diesem Artikel werden wir sowohl grundlegende als auch fortgeschrittene Konzepte der funktionalen Programmierung in Python erkunden.

---

## Inhaltsverzeichnis

1. Einführung in die funktionale Programmierung  
2. Definition von Funktionen in Python  
3. Parameter und Argumente  
4. Rückgabewerte (`return`)  
5. Lambda-Funktionen  
6. Höherwertige Funktionen  
7. Rekursive Funktionen  
8. Eingebaute Python-Funktionen für funktionale Programmierung  
9. Reine Funktionen und Zustandsverwaltung  
10. Fortgeschrittene Tipps und Best Practices  
11. Praktische Übungen  
12. Mini-Projekt: Notensystem  
13. Vergleich mit objektorientierter Programmierung  
14. Funktionstests schreiben  
15. Nützliche Bibliotheken  
16. Häufig gestellte Fragen  
17. Empfohlene Ressourcen  
18. Abschließendes Fazit  

---

## 1. Einführung in die funktionale Programmierung

Funktionale Programmierung ist ein Programmierstil, bei dem Funktionen die Hauptbausteine des Programms sind. In diesem Paradigma werden Daten nicht verändert, sondern durch neue Funktionen verarbeitet.

**Hauptmerkmale:**

- Verwendung reiner Funktionen  
- Vermeidung von Zustandsänderungen  
- Nutzung höherwertiger Funktionen  
- Verwendung von Rekursion  

---

## 2. Definition von Funktionen in Python

In Python werden Funktionen mit dem Schlüsselwort `def` definiert:

```python
def hallo():
    print("Hallo Davood!")
```

Funktionsaufruf:

```python
hallo()
```

---

## 3. Parameter und Argumente

Funktionen können Eingabeparameter akzeptieren:

```python
def addieren(a, b):
    return a + b

ergebnis = addieren(3, 5)
print(ergebnis)  # Ausgabe: 8
```

---

## 4. Rückgabewerte (`return`)

Das Schlüsselwort `return` wird verwendet, um einen Wert aus einer Funktion zurückzugeben:

```python
def quadrat(x):
    return x * x

print(quadrat(4))  # Ausgabe: 16
```

---

## 5. Lambda-Funktionen

Lambda-Funktionen sind anonyme Funktionen, die typischerweise für einfache Operationen verwendet werden:

```python
quadrat = lambda x: x * x
print(quadrat(6))  # Ausgabe: 36
```

Beispiel mit `map`:

```python
zahlen = [1, 2, 3, 4]
quadrate = list(map(lambda x: x * x, zahlen))
print(quadrate)  # Ausgabe: [1, 4, 9, 16]
```

---

## 6. Höherwertige Funktionen

Funktionen, die andere Funktionen als Argumente akzeptieren oder Funktionen zurückgeben.

### `map`

```python
zahlen = [1, 2, 3]
ergebnisse = list(map(lambda x: x + 1, zahlen))
print(ergebnisse)  # Ausgabe: [2, 3, 4]
```

### `filter`

```python
zahlen = [1, 2, 3, 4, 5]
gerade = list(filter(lambda x: x % 2 == 0, zahlen))
print(gerade)  # Ausgabe: [2, 4]
```

### `reduce`

```python
from functools import reduce

zahlen = [1, 2, 3, 4]
summe = reduce(lambda x, y: x + y, zahlen)
print(summe)  # Ausgabe: 10
```

---

## 7. Rekursive Funktionen

Eine Funktion, die sich selbst aufruft:

```python
def fakultaet(n):
    if n == 0:
        return 1
    else:
        return n * fakultaet(n - 1)

print(fakultaet(5))  # Ausgabe: 120
```

---

## 8. Eingebaute Python-Funktionen für funktionale Programmierung

Nützliche eingebaute Funktionen:

- `map()`  
- `filter()`  
- `reduce()`  
- `zip()`  
- `enumerate()`  

Beispiel mit `zip`:

```python
namen = ["Ali", "Zahra", "Davood"]
alter = [25, 30, 28]

kombiniert = list(zip(namen, alter))
print(kombiniert)  # Ausgabe: [('Ali', 25), ('Zahra', 30), ('Davood', 28)]
```

---

## 9. Reine Funktionen und Zustandsverwaltung

Eine reine Funktion hängt nur von ihren Eingaben ab und verursacht keine externen Änderungen.

### Reine Funktion:

```python
def reine_addition(a, b):
    return a + b
```

### Unreine Funktion:

```python
wert = 10

def unreine_addition(x):
    return x + wert
```

---

## 10. Fortgeschrittene Tipps und Best Practices

- Verwende reine Funktionen  
- Vermeide Zustandsänderungen  
- Dokumentiere deine Funktionen  
- Nutze Unit-Tests  
- Verwende höherwertige Funktionen  

---

## 11. Praktische Übungen

### Übung 1: Quadratzahlen

```python
zahlen = [1, 2, 3, 4, 5]
quadrate = list(map(lambda x: x ** 2, zahlen))
print(quadrate)
```

### Übung 2: Zeichenketten filtern

```python
woerter = ["Hallo", "Reise", "Freund", "Uhr"]
gefiltert = list(filter(lambda x: x.startswith("R"), woerter))
print(gefiltert)
```

### Übung 3: Summe der geraden Zahlen

```python
from functools import reduce

zahlen = [1, 2, 3, 4, 5, 6]
gerade = list(filter(lambda x: x % 2 == 0, zahlen))
summe_gerade = reduce(lambda x, y: x + y, gerade)
print(summe_gerade)
```

---

## 12. Mini-Projekt: Notensystem

Natürlich Davood! Hier ist die vollständige Übersetzung ins Deutsche, originalgetreu und im Markdown-Format:

```markdown
```python
from functools import reduce

students = [
    {"name": "Ali", "score": 17},
    {"name": "Zahra", "score": 12},
    {"name": "Davood", "score": 19},
    {"name": "Sara", "score": 9}
]

passed_students = list(filter(lambda x: x["score"] >= 10, students))
passed_scores = list(map(lambda x: x["score"], passed_students))
average = reduce(lambda x, y: x + y, passed_scores) / len(passed_scores)

print("Bestandene Studierende:")
for student in passed_students:
    print(f"{student['name']} mit Note {student['score']}")

print(f"Durchschnittsnote der bestandenen Studierenden: {average}")
```

---

## 13. Vergleich mit objektorientierter Programmierung

| Merkmal         | Funktional                   | Objektorientiert            |
|----------------|------------------------------|-----------------------------|
| Fokus           | Funktionen                   | Objekte und Klassen         |
| Zustandsänderung| Vermeidung                   | Erlaubt                     |
| Lesbarkeit      | Hoch                         | Abhängig vom Design         |
| Testbarkeit     | Einfach                      | Komplexer                   |
| Werkzeuge       | `map`, `filter`, `lambda`    | `class`, `self`             |

---

## 14. Funktionstests in der funktionalen Programmierung

Tests sind eine der wichtigsten Phasen der Softwareentwicklung. In der funktionalen Programmierung sind Funktionen rein und unabhängig vom externen Zustand, was ihre Testbarkeit erheblich vereinfacht.

### Beispiel mit `unittest`

```python
import unittest

def quadrat(x):
    return x * x

class TestFunctions(unittest.TestCase):
    def test_quadrat(self):
        self.assertEqual(quadrat(3), 9)
        self.assertEqual(quadrat(0), 0)
        self.assertEqual(quadrat(-2), 4)

if __name__ == "__main__":
    unittest.main()
```

### Beispiel mit `pytest`

```python
def addieren(a, b):
    return a + b

def test_addieren():
    assert addieren(2, 3) == 5
    assert addieren(-1, 1) == 0
    assert addieren(0, 0) == 0
```

Um Tests mit `pytest` auszuführen, verwende einfach folgenden Befehl im Terminal:

```bash
pytest dateiname.py
```

---

## 15. Nützliche Bibliotheken für funktionale Programmierung

Python bietet Bibliotheken mit fortgeschrittenen Werkzeugen für funktionale Programmierung.

### `functools`

Standardbibliothek von Python für fortgeschrittene Funktionen:

- `reduce`: reduziert eine Liste auf einen einzelnen Wert  
- `partial`: erstellt angepasste Versionen von Funktionen  
- `lru_cache`: speichert Funktionsresultate im Cache  

Beispiel mit `partial`:

```python
from functools import partial

def multiplizieren(a, b):
    return a * b

doppelt = partial(multiplizieren, 2)
print(doppelt(5))  # Ausgabe: 10
```

### `toolz`

Eine leistungsstarke Bibliothek für komplexere funktionale Operationen:

```bash
pip install toolz
```

Beispiel mit `curry`:

```python
from toolz import curry

@curry
def addieren(a, b):
    return a + b

addiere_5 = addieren(5)
print(addiere_5(3))  # Ausgabe: 8
```

---

## 16. Häufig gestellte Fragen

### Ist funktionale Programmierung für große Projekte geeignet?

Ja, vorausgesetzt die Projektstruktur ist gut gestaltet und es werden reine Funktionen verwendet. Dieser Stil reduziert Fehler und verbessert die Testbarkeit.

### Kann funktionale Programmierung mit objektorientierter Programmierung kombiniert werden?

Ja, Python erlaubt die gleichzeitige Nutzung beider Paradigmen. Viele reale Projekte kombinieren beide Ansätze.

### Sind Lambda-Funktionen testbar?

Ja, aber für bessere Testbarkeit empfiehlt es sich, benannte Funktionen zu verwenden, um die Lesbarkeit und das Debugging zu verbessern.

---

## 17. Empfohlene Ressourcen für vertiefendes Lernen

Um tiefer in die funktionale Programmierung mit Python einzutauchen, werden folgende Ressourcen empfohlen:

- [Offizielle Python-Dokumentation](https://docs.python.org)  
- Buch: "Functional Python Programming" von David Mertz  
- Online-Kurse auf Coursera, Udemy und edX  
- Dokumentation der Bibliotheken `toolz` und `functools`  

---

# Übungen zur funktionalen Programmierung in Python

In diesem Abschnitt findest du 10 praktische Übungen zur Stärkung deiner Fähigkeiten in funktionaler Programmierung mit Python. Versuche bei jeder Übung, reine Funktionen, Lambda-Funktionen, höherwertige Funktionen (`map`, `filter`, `reduce`) und Rekursion zu verwenden.

---

## Übung 1: Liste von Zahlen in Liste von Quadraten umwandeln

Du hast eine Liste von Ganzzahlen. Verwende `map` und `lambda`, um eine Liste ihrer Quadrate zu erzeugen.

```python
numbers = [1, 2, 3, 4, 5]
# Erwartete Ausgabe: [1, 4, 9, 16, 25]
```

---

## Übung 2: Zeichenketten filtern, die mit "S" beginnen

Du hast eine Liste von Zeichenketten. Verwende `filter` und `lambda`, um nur diejenigen zu behalten, die mit dem Buchstaben "S" beginnen.

```python
words = ["Hello", "Travel", "Friend", "Clock", "Book"]
# Erwartete Ausgabe: ["Hello", "Travel", "Clock"]
```

---

## Übung 3: Summe der geraden Zahlen mit `reduce` berechnen

Du hast eine Liste von Zahlen. Filtere zuerst nur die geraden Zahlen und verwende dann `reduce`, um deren Summe zu berechnen.

```python
numbers = [1, 2, 3, 4, 5, 6]
# Erwartete Ausgabe: 12
```

---

## Übung 4: Liste von Zeichenketten in Liste ihrer Längen umwandeln

Verwende `map`, um eine Liste der Längen der Zeichenketten aus der ursprünglichen Liste zu erzeugen.

```python
words = ["Python", "Functional", "Programming"]
# Erwartete Ausgabe: [6, 10, 11]
```

---

## Übung 5: Reine Funktionen überprüfen

Schreibe eine Funktion, die zwei Zahlen addiert und keine Abhängigkeit von externen Variablen hat. Überprüfe anschließend, ob deine Funktion rein ist.

```python
def add(a, b):
    # Dein Code hier
```

---

## Übung 6: Verwende `zip`, um zwei Listen zu kombinieren

Du hast zwei Listen: eine mit Namen und eine mit Alter. Verwende `zip`, um eine Liste von (Name, Alter)-Paaren zu erstellen.

```python
names = ["Ali", "Zahra", "Davood"]
ages = [25, 30, 28]
# Erwartete Ausgabe: [('Ali', 25), ('Zahra', 30), ('Davood', 28)]
```

---

## Übung 7: Rekursive Funktion zur Berechnung der Fakultät

Schreibe eine rekursive Funktion zur Berechnung der Fakultät einer Ganzzahl.

```python
def factorial(n):
    # Dein Code hier
```

---

## Übung 8: Verwende `enumerate`, um Listenelemente zu nummerieren

Verwende `enumerate`, um die Elemente einer Liste zu nummerieren und jedes Element als `(Index, Wert)`-Tupel darzustellen.

```python
words = ["Function", "Lambda", "Filter"]
# Erwartete Ausgabe: [(0, "Function"), (1, "Lambda"), (2, "Filter")]
```

---

## Übung 9: Verwende `partial`, um eine benutzerdefinierte Funktion zu erstellen

Verwende `functools.partial`, um eine Funktion zu erstellen, die die Eingabe immer mit 3 multipliziert.

```python
# Erwartete Ausgabe: Eine Funktion, die mit 3 multipliziert
```

---

## Übung 10: Durchschnittsnote im funktionalen Stil berechnen

Du hast eine Liste von Dictionaries mit Namen und Noten von Studierenden. Verwende `map`, `filter` und `reduce`, um die Durchschnittsnote der Studierenden zu berechnen, die mehr als 10 Punkte erzielt haben.

```python
students = [
    {"name": "Ali", "score": 17},
    {"name": "Zahra", "score": 12},
    {"name": "Davood", "score": 19},
    {"name": "Sara", "score": 9}
]
# Erwartete Ausgabe: Durchschnittsnote der bestandenen Studierenden
```

---

## 18. Abschließendes Fazit

Funktionale Programmierung in Python ist ein leistungsstarker, lesbarer und testbarer Stil für die Softwareentwicklung. Durch die Verwendung reiner Funktionen, höherwertiger Funktionen und die Vermeidung von Zustandsänderungen kannst du Code schreiben, der wartbar ist und eine hohe Leistung bietet.

Wenn du darauf abzielst, zuverlässigen, skalierbaren und leicht testbaren Code zu schreiben, ist funktionale Programmierung eine der besten Optionen. Mit Übung und den richtigen Werkzeugen kannst du dieses Paradigma zu einem festen Bestandteil deiner Programmierfähigkeiten machen.



---



# 🇬🇧 Section 3: Functional Programming in Python

Functional programming is one of the powerful programming paradigms that focuses on using pure functions, avoiding state mutation, and leveraging higher-order functions. In this article, we’ll explore both basic and advanced concepts of functional programming in Python.

---

## Table of Contents

1. Introduction to Functional Programming  
2. Defining Functions in Python  
3. Parameters and Arguments  
4. Return Values (`return`)  
5. Lambda Functions  
6. Higher-Order Functions  
7. Recursive Functions  
8. Built-in Python Functions for Functional Programming  
9. Pure Functions and State Management  
10. Advanced Tips and Best Practices  
11. Practical Exercises  
12. Mini Project: Grading System  
13. Comparison with Object-Oriented Programming  
14. Writing Tests for Functions  
15. Useful Libraries  
16. Frequently Asked Questions  
17. Recommended Resources  
18. Final Conclusion  

---

## 1. Introduction to Functional Programming

Functional programming is a style of programming where functions are the main building blocks of the program. In this paradigm, data is not mutated but processed through new functions.

**Key Features:**

- Use of pure functions  
- Avoiding state mutation  
- Use of higher-order functions  
- Use of recursion  

---

## 2. Defining Functions in Python

In Python, functions are defined using the `def` keyword:

```python
def hello():
    print("Hello Davood!")
```

Calling the function:

```python
hello()
```

---

## 3. Parameters and Arguments

Functions can accept input parameters:

```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # Output: 8
```

---

## 4. Return Values (`return`)

The `return` keyword is used to return a value from a function:

```python
def square(x):
    return x * x

print(square(4))  # Output: 16
```

---

## 5. Lambda Functions

Lambda functions are anonymous functions typically used for simple operations:

```python
square = lambda x: x * x
print(square(6))  # Output: 36
```

Example with `map`:

```python
numbers = [1, 2, 3, 4]
squares = list(map(lambda x: x * x, numbers))
print(squares)  # Output: [1, 4, 9, 16]
```

---

## 6. Higher-Order Functions

Functions that take other functions as arguments or return functions.

### `map`

```python
numbers = [1, 2, 3]
results = list(map(lambda x: x + 1, numbers))
print(results)  # Output: [2, 3, 4]
```

### `filter`

```python
numbers = [1, 2, 3, 4, 5]
evens = list(filter(lambda x: x % 2 == 0, numbers))
print(evens)  # Output: [2, 4]
```

### `reduce`

```python
from functools import reduce

numbers = [1, 2, 3, 4]
total = reduce(lambda x, y: x + y, numbers)
print(total)  # Output: 10
```

---

## 7. Recursive Functions

A function that calls itself:

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))  # Output: 120
```

---

## 8. Built-in Python Functions for Functional Programming

Useful built-in functions:

- `map()`  
- `filter()`  
- `reduce()`  
- `zip()`  
- `enumerate()`  

Example with `zip`:

```python
names = ["Ali", "Zahra", "Davood"]
ages = [25, 30, 28]

combined = list(zip(names, ages))
print(combined)  # Output: [('Ali', 25), ('Zahra', 30), ('Davood', 28)]
```

---

## 9. Pure Functions and State Management

A pure function depends only on its inputs and does not cause any external changes.

### Pure Function:

```python
def pure_add(a, b):
    return a + b
```

### Impure Function:

```python
value = 10

def impure_add(x):
    return x + value
```

---

## 10. Advanced Tips and Best Practices

- Use pure functions  
- Avoid state mutation  
- Document your functions  
- Use unit testing  
- Leverage higher-order functions  

---

## 11. Practical Exercises

### Exercise 1: Square Numbers

```python
numbers = [1, 2, 3, 4, 5]
squares = list(map(lambda x: x ** 2, numbers))
print(squares)
```

### Exercise 2: Filter Strings

```python
words = ["Hello", "Travel", "Friend", "Clock"]
filtered = list(filter(lambda x: x.startswith("T"), words))
print(filtered)
```

### Exercise 3: Sum of Even Numbers

```python
from functools import reduce

numbers = [1, 2, 3, 4, 5, 6]
evens = list(filter(lambda x: x % 2 == 0, numbers))
sum_evens = reduce(lambda x, y: x + y, evens)
print(sum_evens)
```

---

## 12. Mini Project: Grading System

```python
from functools import reduce

students = [
    {"name": "Ali", "score": 17},
    {"name": "Zahra", "score": 12},
    {"name": "Davood", "score": 19},
    {"name": "Sara", "score": 9}
]

passed_students = list(filter(lambda x: x["score"] >= 10, students))
passed_scores = list(map(lambda x: x["score"], passed_students))
average = reduce(lambda x, y: x + y, passed_scores) / len(passed_scores)

print("Passed Students:")
for student in passed_students:
    print(f"{student['name']} with score {student['score']}")

print(f"Average score of passed students: {average}")
```

---

## 13. Comparison with Object-Oriented Programming

| Feature         | Functional                   | Object-Oriented             |
|----------------|------------------------------|-----------------------------|
| Focus           | Functions                    | Objects and Classes         |
| State Mutation  | Avoided                      | Allowed                     |
| Readability     | High                         | Depends on design           |
| Testability     | Easy                         | More complex                |
| Tools           | `map`, `filter`, `lambda`    | `class`, `self`             |

---

## 14. Function Testing in Functional Programming

Testing is one of the most important stages of software development. In functional programming, since functions are pure and don’t rely on external state, they are much easier to test.

### Example with `unittest`

```python
import unittest

def square(x):
    return x * x

class TestFunctions(unittest.TestCase):
    def test_square(self):
        self.assertEqual(square(3), 9)
        self.assertEqual(square(0), 0)
        self.assertEqual(square(-2), 4)

if __name__ == "__main__":
    unittest.main()
```

### Example with `pytest`

```python
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
    assert add(-1, 1) == 0
    assert add(0, 0) == 0
```

To run tests with `pytest`, simply execute the following command in the terminal:

```bash
pytest filename.py
```

---

## 15. Useful Libraries for Functional Programming

Python provides libraries that offer advanced tools for functional programming.

### `functools`

Python’s standard library for advanced function utilities:

- `reduce`: to reduce a list to a single value  
- `partial`: to create customized versions of functions  
- `lru_cache`: to cache function results  

Example with `partial`:

```python
from functools import partial

def multiply(a, b):
    return a * b

double = partial(multiply, 2)
print(double(5))  # Output: 10
```

### `toolz`

A powerful library for more complex functional operations:

```bash
pip install toolz
```

Example with `curry`:

```python
from toolz import curry

@curry
def add(a, b):
    return a + b

add_5 = add(5)
print(add_5(3))  # Output: 8
```

---

## 16. Frequently Asked Questions

### Is Functional Programming Suitable for Large Projects?

Yes, provided the project structure is well-designed and pure functions are used. This style reduces errors and improves testability.

### Can Functional Programming Be Combined with Object-Oriented Programming?

Yes, Python allows you to use both paradigms together. Many real-world projects are a combination of both.

### Are Lambda Functions Testable?

Yes, but for better testability, it's recommended to use named functions to improve readability and debugging.

---

## 17. Recommended Resources for Further Learning

To dive deeper into functional programming in Python, the following resources are recommended:

- [Official Python Documentation](https://docs.python.org)  
- Book: "Functional Python Programming" by David Mertz  
- Online courses on Coursera, Udemy, and edX  
- Documentation for `toolz` and `functools` libraries  

---

# Functional Programming Exercises in Python

In this section, 10 practical exercises are provided to strengthen your functional programming skills in Python. For each exercise, try to use pure functions, lambda functions, higher-order functions (`map`, `filter`, `reduce`), and recursion.

---

## Exercise 1: Convert List of Numbers to List of Squares

You have a list of integers. Use `map` and `lambda` to generate a list of their squares.

```python
numbers = [1, 2, 3, 4, 5]
# Expected output: [1, 4, 9, 16, 25]
```

---

## Exercise 2: Filter Strings Starting with "S"

You have a list of strings. Use `filter` and `lambda` to keep only those that start with the letter "S".

```python
words = ["Hello", "Travel", "Friend", "Clock", "Book"]
# Expected output: ["Hello", "Travel", "Clock"]
```

---

## Exercise 3: Calculate Sum of Even Numbers with `reduce`

You have a list of numbers. First, filter only the even numbers, then use `reduce` to calculate their sum.

```python
numbers = [1, 2, 3, 4, 5, 6]
# Expected output: 12
```

---

## Exercise 4: Convert List of Strings to List of Their Lengths

Use `map` to generate a list of string lengths from the original list.

```python
words = ["Python", "Functional", "Programming"]
# Expected output: [6, 10, 11]
```

---

## Exercise 5: Check for Pure Functions

Write a function that adds two numbers and has no dependency on external variables. Then verify whether your function is pure.

```python
def add(a, b):
    # Your code here
```

---

## Exercise 6: Use `zip` to Combine Two Lists

You have two lists: one with names and one with ages. Use `zip` to create a list of (name, age) pairs.

```python
names = ["Ali", "Zahra", "Davood"]
ages = [25, 30, 28]
# Expected output: [('Ali', 25), ('Zahra', 30), ('Davood', 28)]
```

---

## Exercise 7: Recursive Function to Calculate Factorial

Write a recursive function to calculate the factorial of an integer.

```python
def factorial(n):
    # Your code here
```

---

## Exercise 8: Use `enumerate` to Number List Elements

Use `enumerate` to number the elements of a list and display each item as a `(index, value)` tuple.

```python
words = ["Function", "Lambda", "Filter"]
# Expected output: [(0, "Function"), (1, "Lambda"), (2, "Filter")]
```

---

## Exercise 9: Use `partial` to Create a Custom Function

Use `functools.partial` to create a function that always multiplies the input by 3.

```python
# Expected output: A function that multiplies by 3
```

---

## Exercise 10: Calculate Average Score Using Functional Style

You have a list of dictionaries containing student names and scores. Use `map`, `filter`, and `reduce` to calculate the average score of students who scored above 10.

```python
students = [
    {"name": "Ali", "score": 17},
    {"name": "Zahra", "score": 12},
    {"name": "Davood", "score": 19},
    {"name": "Sara", "score": 9}
]
# Expected output: Average score of passed students
```

---

## 18. Final Conclusion

Functional programming in Python is a powerful, readable, and testable style for software development. By using pure functions, higher-order functions, and avoiding state mutation, you can write code that is maintainable and performs well.

If you're aiming to write code that is reliable, scalable, and easy to test, functional programming is one of the best choices. With practice and the right tools, you can make this paradigm an integral part of your programming skillset.



---



# 🇮🇷 برنامه‌نویسی تابعی در پایتون

برنامه‌نویسی تابعی (Functional Programming) یکی از سبک‌های قدرتمند برنامه‌نویسی است که تمرکز آن بر استفاده از توابع خالص، اجتناب از تغییر وضعیت (state)، و بهره‌گیری از توابع مرتبه بالا است. در این مقاله، با مفاهیم پایه و پیشرفته‌ی برنامه‌نویسی تابعی در پایتون آشنا می‌شویم.

--- 

## فهرست مطالب

1. مقدمه‌ای بر برنامه‌نویسی تابعی  
2. تعریف تابع در پایتون  
3. پارامترها و آرگومان‌ها  
4. مقدار بازگشتی (`return`)  
5. توابع لامبدا (Lambda)  
6. توابع مرتبه بالا (Higher-Order Functions)  
7. توابع بازگشتی (Recursive Functions)  
8. توابع داخلی پایتون برای برنامه‌نویسی تابعی  
9. توابع خالص و مدیریت وضعیت  
10. نکات پیشرفته و بهترین تمرین‌ها  
11. تمرین‌های عملی  
12. پروژه‌ی کوچک: سیستم نمره‌دهی  
13. مقایسه با برنامه‌نویسی شی‌گرا  
14. تست‌نویسی توابع  
15. کتابخانه‌های مفید  
16. سوالات متداول  
17. منابع پیشنهادی  
18. نتیجه‌گیری نهایی  

---

## 1. مقدمه‌ای بر برنامه‌نویسی تابعی

برنامه‌نویسی تابعی سبکی از برنامه‌نویسی است که در آن توابع به عنوان واحدهای اصلی ساختار برنامه استفاده می‌شوند. در این سبک، داده‌ها تغییر نمی‌کنند بلکه از طریق توابع جدید پردازش می‌شوند.

**ویژگی‌های اصلی:**

- استفاده از توابع خالص  
- اجتناب از تغییر وضعیت  
- استفاده از توابع مرتبه بالا  
- استفاده از بازگشت (Recursion)  

---

## 2. تعریف تابع در پایتون

در پایتون، تابع با استفاده از کلیدواژه `def` تعریف می‌شود:

```python
def سلام():
    print("سلام داوود!")
```

فراخوانی تابع:

```python
سلام()
```

---

## 3. پارامترها و آرگومان‌ها

توابع می‌توانند ورودی دریافت کنند:

```python
def جمع(a, b):
    return a + b

نتیجه = جمع(3, 5)
print(نتیجه)  # خروجی: 8
```

---

## 4. مقدار بازگشتی (`return`)

کلمه‌ی کلیدی `return` برای بازگرداندن مقدار از تابع استفاده می‌شود:

```python
def مربع(x):
    return x * x

print(مربع(4))  # خروجی: 16
```

---

## 5. توابع لامبدا (Lambda)

توابع لامبدا، توابعی بدون نام هستند که معمولاً برای عملیات‌های ساده استفاده می‌شوند:

```python
مربع = lambda x: x * x
print(مربع(6))  # خروجی: 36
```

مثال با `map`:

```python
اعداد = [1, 2, 3, 4]
مربعات = list(map(lambda x: x * x, اعداد))
print(مربعات)  # خروجی: [1, 4, 9, 16]
```

---

## 6. توابع مرتبه بالا (Higher-Order Functions)

توابعی هستند که توابع دیگر را به عنوان آرگومان دریافت می‌کنند یا تابعی را بازمی‌گردانند.

### `map`

```python
اعداد = [1, 2, 3]
نتایج = list(map(lambda x: x + 1, اعداد))
print(نتایج)  # خروجی: [2, 3, 4]
```

### `filter`

```python
اعداد = [1, 2, 3, 4, 5]
زوج‌ها = list(filter(lambda x: x % 2 == 0, اعداد))
print(زوج‌ها)  # خروجی: [2, 4]
```

### `reduce`

```python
from functools import reduce

اعداد = [1, 2, 3, 4]
جمع = reduce(lambda x, y: x + y, اعداد)
print(جمع)  # خروجی: 10
```

---

## 7. توابع بازگشتی (Recursive Functions)

تابعی که خودش را فراخوانی می‌کند:

```python
def فاکتوریل(n):
    if n == 0:
        return 1
    else:
        return n * فاکتوریل(n - 1)

print(فاکتوریل(5))  # خروجی: 120
```

---

## 8. توابع داخلی پایتون برای برنامه‌نویسی تابعی

توابع داخلی مفید:

- `map()`  
- `filter()`  
- `reduce()`  
- `zip()`  
- `enumerate()`  

مثال با `zip`:

```python
نام‌ها = ["علی", "زهرا", "داوود"]
سن‌ها = [25, 30, 28]

ترکیب = list(zip(نام‌ها, سن‌ها))
print(ترکیب)  # خروجی: [('علی', 25), ('زهرا', 30), ('داوود', 28)]
```

---

## 9. توابع خالص و مدیریت وضعیت

تابع خالص فقط به ورودی‌های خود وابسته است و هیچ تغییر خارجی ایجاد نمی‌کند.

### تابع خالص:

```python
def جمع_خالص(a, b):
    return a + b
```

### تابع غیرخالص:

```python
مقدار = 10

def جمع_غیرخالص(x):
    return x + مقدار
```

---

## 10. نکات پیشرفته و بهترین تمرین‌ها

- از توابع خالص استفاده کنید  
- از تغییر وضعیت اجتناب کنید  
- توابع را مستندسازی کنید  
- از تست واحد استفاده کنید  
- از توابع مرتبه بالا بهره ببرید  

---

## 11. تمرین‌های عملی

### تمرین ۱: مربع اعداد

```python
اعداد = [1, 2, 3, 4, 5]
مربعات = list(map(lambda x: x ** 2, اعداد))
print(مربعات)
```

### تمرین ۲: فیلتر رشته‌ها

```python
کلمات = ["سلام", "سفر", "دوست", "ساعت"]
فیلترشده = list(filter(lambda x: x.startswith("س"), کلمات))
print(فیلترشده)
```

### تمرین ۳: مجموع زوج‌ها

```python
from functools import reduce

اعداد = [1, 2, 3, 4, 5, 6]
زوج‌ها = list(filter(lambda x: x % 2 == 0, اعداد))
جمع_زوج‌ها = reduce(lambda x, y: x + y, زوج‌ها)
print(جمع_زوج‌ها)
```

---

## 12. پروژه‌ی کوچک: سیستم نمره‌دهی

```python
from functools import reduce

دانش‌آموزان = [
    {"نام": "علی", "نمره": 17},
    {"نام": "زهرا", "نمره": 12},
    {"نام": "داوود", "نمره": 19},
    {"نام": "سارا", "نمره": 9}
]

قبول‌شده‌ها = list(filter(lambda x: x["نمره"] >= 10, دانش‌آموزان))
نمرات_قبول = list(map(lambda x: x["نمره"], قبول‌شده‌ها))
میانگین = reduce(lambda x, y: x + y, نمرات_قبول) / len(nمرات_قبول)

print("دانش‌آموزان قبول‌شده:")
for دانش‌آموز in قبول‌شده‌ها:
    print(f"{دانش‌آموز['نام']} با نمره {دانش‌آموز['نمره']}")

print(f"میانگین نمرات قبول‌شده: {میانگین}")
```

---

## 13. مقایسه با برنامه‌نویسی شی‌گرا

| ویژگی           | تابعی                        | شی‌گرا                      |
|----------------|------------------------------|-----------------------------|
| تمرکز          | توابع                        | اشیاء و کلاس‌ها            |
| تغییر وضعیت    | اجتناب از آن                 | مجاز                        |
| خوانایی        | بالا                         | وابسته به طراحی            |
| تست‌پذیری      | آسان                         | پیچیده‌تر                   |
| ابزارها        | `map`, `filter`, `lambda`    | `class`, `self`             |

---

## 14. تست‌نویسی توابع تابعی

تست‌نویسی یکی از مهم‌ترین مراحل توسعه نرم‌افزار است. در برنامه‌نویسی تابعی، چون توابع خالص هستند و وابستگی به وضعیت خارجی ندارند، تست‌پذیری آن‌ها بسیار ساده‌تر است.

### مثال با `unittest`

```python
import unittest

def مربع(x):
    return x * x

class TestFunctions(unittest.TestCase):
    def test_مربع(self):
        self.assertEqual(مربع(3), 9)
        self.assertEqual(مربع(0), 0)
        self.assertEqual(مربع(-2), 4)

if __name__ == "__main__":
    unittest.main()
```

### مثال با `pytest`

```python
def جمع(a, b):
    return a + b

def test_جمع():
    assert جمع(2, 3) == 5
    assert جمع(-1, 1) == 0
    assert جمع(0, 0) == 0
```

برای اجرای تست‌ها با `pytest` کافیست دستور زیر را در ترمینال اجرا کنید:

```bash
pytest نام_فایل.py
```

---

## 15. کتابخانه‌های مفید برای برنامه‌نویسی تابعی

پایتون کتابخانه‌هایی دارد که ابزارهای پیشرفته‌تری برای برنامه‌نویسی تابعی فراهم می‌کنند.

### `functools`

کتابخانه‌ی استاندارد پایتون برای توابع پیشرفته:

- `reduce`: برای کاهش لیست به یک مقدار
- `partial`: برای ساخت نسخه‌های سفارشی از توابع
- `lru_cache`: برای کش کردن نتایج توابع

مثال با `partial`:

```python
from functools import partial

def ضرب(a, b):
    return a * b

دوبرابر = partial(ضرب, 2)
print(دوبرابر(5))  # خروجی: 10
```

### `toolz`

کتابخانه‌ای قدرتمند برای عملیات‌های تابعی پیچیده‌تر:

```bash
pip install toolz
```

مثال با `curry`:

```python
from toolz import curry

@curry
def جمع(a, b):
    return a + b

جمع_با_۵ = جمع(5)
print(جمع_با_۵(3))  # خروجی: 8
```

---

## 16. سوالات متداول

### آیا برنامه‌نویسی تابعی برای پروژه‌های بزرگ مناسب است؟

بله، به شرطی که ساختار پروژه به خوبی طراحی شده باشد و از توابع خالص استفاده شود. این سبک باعث کاهش خطا و افزایش تست‌پذیری می‌شود.

### آیا می‌توان برنامه‌نویسی تابعی را با شی‌گرا ترکیب کرد؟

بله، پایتون اجازه می‌دهد از هر دو سبک در کنار هم استفاده کنید. بسیاری از پروژه‌های واقعی ترکیبی از این دو هستند.

### آیا توابع لامبدا قابل تست هستند؟

بله، ولی بهتر است برای تست‌پذیری بیشتر از توابع معمولی با نام مشخص استفاده شود تا خوانایی و قابلیت اشکال‌زدایی افزایش یابد.

---

## 17. منابع پیشنهادی برای یادگیری بیشتر

برای یادگیری عمیق‌تر برنامه‌نویسی تابعی در پایتون، منابع زیر پیشنهاد می‌شوند:

- [مستندات رسمی پایتون](https://docs.python.org)
- کتاب "Functional Python Programming" نوشته David Mertz
- دوره‌های آموزشی در Coursera، Udemy و edX
- مستندات کتابخانه‌های `toolz` و `functools`

---

# تمرین‌های برنامه‌نویسی تابعی در پایتون

در این بخش، ۱۰ تمرین عملی برای تقویت مهارت‌های برنامه‌نویسی تابعی در پایتون ارائه شده‌اند. برای حل هر تمرین، سعی کنید از توابع خالص، توابع لامبدا، توابع مرتبه بالا (`map`, `filter`, `reduce`) و بازگشت استفاده کنید.

---

## تمرین ۱: تبدیل لیست اعداد به لیست مربع‌ها

لیستی از اعداد صحیح دارید. با استفاده از `map` و `lambda`، لیستی از مربع این اعداد تولید کنید.

```python
اعداد = [1, 2, 3, 4, 5]
# خروجی مورد انتظار: [1, 4, 9, 16, 25]
```

---

## تمرین ۲: فیلتر کردن رشته‌هایی که با حرف "س" شروع می‌شوند

لیستی از رشته‌ها دارید. با استفاده از `filter` و `lambda`، فقط رشته‌هایی را نگه دارید که با حرف "س" شروع می‌شوند.

```python
کلمات = ["سلام", "سفر", "دوست", "ساعت", "کتاب"]
# خروجی مورد انتظار: ["سلام", "سفر", "ساعت"]
```

---

## تمرین ۳: محاسبه مجموع اعداد زوج با `reduce`

لیستی از اعداد دارید. ابتدا فقط اعداد زوج را فیلتر کنید، سپس با `reduce` مجموع آن‌ها را محاسبه کنید.

```python
اعداد = [1, 2, 3, 4, 5, 6]
# خروجی مورد انتظار: 12
```

---

## تمرین ۴: تبدیل لیست رشته‌ها به لیست طول آن‌ها

با استفاده از `map`، لیستی از طول رشته‌ها را از لیست اولیه تولید کنید.

```python
کلمات = ["پایتون", "تابعی", "برنامه‌نویسی"]
# خروجی مورد انتظار: [6, 5, 13]
```

---

## تمرین ۵: بررسی توابع خالص

تابعی بنویسید که دو عدد را جمع کند و هیچ وابستگی به متغیرهای خارجی نداشته باشد. سپس بررسی کنید که آیا تابع شما خالص است یا نه.

```python
def جمع(a, b):
    # کد شما
```

---

## تمرین ۶: استفاده از `zip` برای ترکیب دو لیست

دو لیست دارید: یکی شامل نام‌ها و دیگری شامل سن‌ها. با استفاده از `zip`، لیستی از زوج‌های (نام، سن) بسازید.

```python
نام‌ها = ["علی", "زهرا", "داوود"]
سن‌ها = [25, 30, 28]
# خروجی مورد انتظار: [('علی', 25), ('زهرا', 30), ('داوود', 28)]
```

---

## تمرین ۷: تابع بازگشتی برای محاسبه فاکتوریل

تابعی بازگشتی بنویسید که فاکتوریل یک عدد صحیح را محاسبه کند.

```python
def فاکتوریل(n):
    # کد شما
```

---

## تمرین ۸: استفاده از `enumerate` برای شماره‌گذاری عناصر لیست

با استفاده از `enumerate`، لیستی از رشته‌ها را شماره‌گذاری کنید و هر عنصر را به صورت `(شماره، رشته)` نمایش دهید.

```python
کلمات = ["تابع", "لامبدا", "فیلتر"]
# خروجی مورد انتظار: [(0, "تابع"), (1, "لامبدا"), (2, "فیلتر")]
```

---

## تمرین ۹: استفاده از `partial` برای ساخت تابع سفارشی

با استفاده از `functools.partial`، تابعی بسازید که همیشه عدد ورودی را در ۳ ضرب کند.

```python
# خروجی مورد انتظار: تابعی که ضرب در ۳ انجام می‌دهد
```

---

## تمرین ۱۰: محاسبه میانگین نمرات با سبک تابعی

لیستی از دیکشنری‌ها دارید که شامل نام و نمره دانش‌آموزان است. با استفاده از `map`, `filter`, و `reduce` میانگین نمرات دانش‌آموزانی را محاسبه کنید که نمره‌شان بالای ۱۰ است.

```python
دانش‌آموزان = [
    {"نام": "علی", "نمره": 17},
    {"نام": "زهرا", "نمره": 12},
    {"نام": "داوود", "نمره": 19},
    {"نام": "سارا", "نمره": 9}
]
# خروجی مورد انتظار: میانگین نمرات قبول‌شده
```

---

## 18. نتیجه‌گیری نهایی

برنامه‌نویسی تابعی در پایتون یک سبک قدرتمند، خوانا و قابل تست برای توسعه نرم‌افزار است. با استفاده از توابع خالص، توابع مرتبه بالا، و اجتناب از تغییر وضعیت، می‌توان کدهایی نوشت که هم قابل نگهداری باشند و هم عملکرد بالایی داشته باشند.

اگر به دنبال نوشتن کدی هستید که قابل اعتماد، قابل توسعه و قابل تست باشد، برنامه‌نویسی تابعی یکی از بهترین انتخاب‌هاست. با تمرین و استفاده از ابزارهای مناسب، می‌توانید این سبک را به بخشی جدایی‌ناپذیر از مهارت‌های برنامه‌نویسی خود تبدیل کنید.

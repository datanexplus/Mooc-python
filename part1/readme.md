# Python MOOC 2025 – Parte 1 🚀  
Chuleta de los fragmentos y conceptos más usados en los ejercicios

---

## 1. Getting started — primeros programas

```python
# tu primer programa
print("Hi there!")

# varias líneas se ejecutan de arriba hacia abajo
print("Welcome to Introduction to Programming!")
print("First we will practise using the print command.")
print("This program prints three lines of text on the screen.")

# operaciones aritméticas dentro de print
print(2 + 5)           # 7
print(3 * 3)           # 9
print(2 + 2 * 10)      # 22

# comentarios (no se ejecutan)
print("Hours in a year:")
# 365 días * 24 h
print(365 * 24)
```
Puntos clave

Usa comillas para strings, sin comillas para operaciones.

Cualquier línea que empiece con # es un comentario.

## 2. Information from the user - leyendo input

```python
name = input("What is your name? ")
print("Hi there, " + name)

# combinar varias veces la misma variable
print("Hi " + name + "! Let me make sure: your name is " + name + "?")

# múltiples entradas
email    = input("What is your email address? ")
nickname = input("What is your nickname? ")
print("Let's make sure we got this right")
print("Your email address: " + email)
```
Puntos clave

input() siempre devuelve str.

Concatenar cadenas se hace con +.

## 3. More about variables - tipos, casting, f-strings

```python
# concatenar strings guardados en variables
given_name  = "Paul"
family_name = "Python"
name = given_name + " " + family_name
print(name)                        # Paul Python

# cambiar el valor (¡es variable!)
word = input("Please type in a word: ")
word = word + "!!!"
print(word)

# diferencias entre str e int
number1 = 100        # int
number2 = "100"      # str
print(number1 + number1)   # 200
print(number2 + number2)   # 100100

# casting y f-strings
result = 10 * 25
print("The result is " + str(result))   # vía str()
print(f"The result is {result}")        # vía f-string

# flotantes y media
a, b, c = 2.5, -1.25, 3.62
mean = (a + b + c) / 3
print(f"Mean: {mean}")
```
Puntos clave

Tipos básicos: str, int, float.

Para imprimir mezcla de tipos usa str(), coma en print, o f-strings.

## 4. Arithmetic operations - operadores y entrada numerica

```python
# precedencia y paréntesis
print(2 + 3 * 3)      # 11
print((2 + 3) * 3)    # 15

# división normal vs. entera
x, y = 3, 2
print(x / y)   # 1.5  (float)
print(x // y)  # 1    (int truncado)

# leer números directamente
year = int(input("Which year were you born? "))
print(f"Your age at the end of 2025: {2025 - year}")

# BMI con float()
height = float(input("Height in cm? ")) / 100
weight = float(input("Weight in kg? "))
bmi = weight / height ** 2
print(f"The BMI is {bmi}")

# acumuladores y +=
total = 0
total += int(input("First number: "))
total += int(input("Second number: "))
total += int(input("Third number: "))
print(f"The sum is {total}")
```
Puntos clave

Operadores: + - * / // % **.

Convierte entrada con int() o float().

+=, -=, *= simplifican acumuladores.

## 5. Conditional statements - if, comparacion, booleanos

```python
age = int(input("How old are you? "))

if age > 17:
    print("You are of age!")
    print("Here's a copy of GTA6 for you.")

print("Next customer, please!")

# varios resultados
num = int(input("Please type in a number: "))
if num < 0:
    print("Negative")
if num > 0:
    print("Positive")
if num == 0:
    print("Zero")

# booleanos explícitos
a = 3
condition = a < 5          # True
if condition:
    print("a is less than 5")
```
Puntos clave

Sintaxis: if condición: + dos puntos; el bloque se define con indentación.

Operadores: == != > >= < <=.

Booleanos son True o False.






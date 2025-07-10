````markdown
# Python MOOC 2025 – Parte 2 📚  
Chuleta de fragmentos y conceptos clave para los ejercicios

---

## 1. Programming terminology — statements, expressions, `type()`

```python
# expresión dentro de una sentencia
result = 3 * 4 + 2 ** 2      # 20
print(result)

# inspeccionar tipo de dato
print(type("Anna"))          # <class 'str'>
print(type(result))          # <class 'int'>
````

*Puntos clave*

* Una **sentencia** (statement) ejecuta una acción completa.
* Una **expresión** produce un valor; puede vivir dentro de una sentencia.
* `type(objeto)` devuelve la clase (`int`, `str`, etc.) del argumento.

---

## 2. More conditionals — `if / elif / else`, paridad, comparación

```python
num = int(input("Número: "))

if num % 2 == 0:
    print("even")
else:
    print("odd")

goals_h = int(input("Home goals: "))
goals_a = int(input("Away goals: "))

if goals_h > goals_a:
    print("Home wins")
elif goals_a > goals_h:
    print("Away wins")
else:
    print("Draw")
```

*Puntos clave*

* `%` es el operador **módulo** (resto); `% 2` sirve para detectar par/impar.
* `elif` permite múltiples ramas mutuamente exclusivas.
* `else` se ejecuta sólo si todas las condiciones anteriores son falsas.

---

## 3. Combining conditions — `and`, `or`, `not`, rangos encadenados

```python
age = int(input("Edad: "))

# rango permitido salvo los 25
if 18 <= age <= 30 and age != 25:
    print("Rango permitido")

# validar que la edad esté dentro de 0-120
if not (age < 0 or age > 120):
    print("Edad válida")
```

*Puntos clave*

* Operadores lógicos: `and`, `or`, `not`.
* Se pueden **encadenar comparaciones** (`18 <= age <= 30`).
* `not (condición)` invierte el valor booleano.

---

## 4. Simple loops — `while`, `break`, `continue`, contadores

```python
# bucle indeterminado con salida por -1
while True:
    val = int(input("(-1 para salir): "))
    if val == -1:
        break
    print(val ** 2)

# validador de PIN con máximo de 3 intentos
PIN_OK = "1234"
tries = 0

while tries < 3:
    if input("PIN: ") == PIN_OK:
        print("Acceso concedido")
        break
    tries += 1
else:                       # se ejecuta si no hubo break
    print("Tarjeta bloqueada")
```

*Puntos clave*

* `while True` crea un bucle «infinito» que se corta con `break`.
* `continue` salta al siguiente ciclo sin ejecutar lo que reste del bloque.
* El bloque `else` de un `while` se ejecuta sólo si el lazo termina **sin** `break`.

---

````markdown
# Python MOOC 2025 – Parte 3 🧩  
Chuleta de fragmentos y conceptos clave para los ejercicios

---

## 1. Loops with conditions — inicializar · condición · update

```python
start = int(input("Comienzo: "))

while start <= 10:        # condición
    print(start)
    start += 1            # update
print("Fin del conteo")
````

*Puntos clave*

* Un bucle bien formado tiene **tres pasos**:

  1. **Inicializar** la variable de control.
  2. **Comprobar** la condición en `while`.
  3. **Actualizar** la variable dentro del bloque (para evitar bucle infinito).

---

## 2. Working with strings — concatenación, repetición, slicing

```python
word = "banana"

print(word * 3)           # bananabananabanana
print(word[0], word[-1])  # b a
print(word[1:4])          # ana
print(len(word))          # 6
```

### Ejemplo: pirámide con `*`

```python
rows = 5
for i in range(rows):
    print(" " * (rows - i - 1) + "*" * (2 * i + 1))
```

*Puntos clave*

* `word[index]` accede a un carácter (índices negativos cuentan desde el final).
* `word[a:b]` devuelve una **slice** (subcadena).
* Operadores de string:

  * `+` concatena.
  * `* n` repite.

---

## 3. More loops — `break`, `continue`, bucles anidados

```python
suma = 0
while True:
    x = int(input("(-1 sale): "))
    if x == -1:
        break           # corta el while exterior
    if x >= 10:
        continue        # salta esta iteración
    suma += x
print("Total:", suma)
```

### Bucle anidado (cuenta atrás por cada número)

```python
n = int(input("Cuenta atrás desde: "))

while n > 0:
    m = n
    while m > 0:
        print(m, end=" ")
        m -= 1
    print()
    n -= 1
```

*Puntos clave*

* `break` sale del bucle actual.
* `continue` salta al **siguiente** ciclo del mismo bucle.
* Bucles anidados ⇒ el `break` solo afecta al bucle donde se ejecuta.

---

## 4. Defining functions — `def`, parámetros, `return`

```python
def squared(x):
    """Devuelve x al cuadrado."""
    return x * x

def greet(name="friend"):
    print(f"Hello, {name}!")

# bloque de prueba local
if __name__ == "__main__":
    greet("Emily")
    print(squared(5))      # 25
```

*Puntos clave*

* `def nombre(parámetros):` + **indentación** para el cuerpo.
* `return` envía un valor al llamador; sin `return` la función devuelve `None`.
* Parámetros con valor por defecto (`name="friend"`) son opcionales al llamar.
* `if __name__ == "__main__":` ejecuta pruebas solo cuando corres el archivo directo, no cuando lo importas.

---

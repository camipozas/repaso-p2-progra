---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
background: https://images.unsplash.com/photo-1555109307-f7d9da25c244
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
---

# Repaso P2

Camila Pozas

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/camipozas" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>


---
layout: image-right
image: https://images.unsplash.com/photo-1541336032412-2048a678540d
---

# Ciclo While
El bucle `while` evalúa una condición y luego ejecuta un bloque de código si la condición es verdadera. El bloque de código se ejecuta repetidamente hasta que la condición llega ser o es falsa.

La sintaxis básica es:
```python
contador = 0
while contador < 10:
   # Ejecuta el bloque de código aquí
   # Siempre que el contador sea inferior a 10
```

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Ejemplo 1

```python
dia = 0    
semana = ['Lunes', 'Martes', 'Miércoles', 'Jueves', 'Viernes', 'Sabado', 'Domingo']
while dia < 7:
   print("Hoy es " + semana[dia])
   dia += 1
```
Resultado:
```bash{1|2|3|4|5|6|7}
Hoy es Lunes
Hoy es Martes
Hoy es Miércoles
Hoy es Jueves
Hoy es Viernes
Hoy es Sabado
Hoy es Domingo
```

Aquí más ejercicios: [Ejercicios while 1](http://patriciaemiguel.com/ejercicios/python/2019/03/10/ejercicios-buclewhile-python.html), [Ejercicios while 2](https://www.mclibre.org/consultar/python/ejercicios/ej-while-1.html)
<!-- 
1. La variable "dia" tiene el valor 0.
2. La variable semana es asignada a una lista que contiene todos los días de la semana.
3. El bucle while comienza
4. El bloque de código se ejecutará hasta que la condición devuelva "true".
5. La condición es 'dia < 7' que aproximadamente dice que se ejecute el bucle while hasta que la variable dia sea menor que 7.
6. Así que cuando el dia=7 el bucle while deja de ejecutarse.
7. La variable dia se actualiza en cada iteración.
8. Cuando el bucle while se ejecuta por primera vez, la línea "Hoy es lunes" se imprime en la consola y la variable dia se hace igual a 1.
9. Como la variable dia es igual a 1 y es menor que 7, se ejecuta de nuevo el bucle while.
10. Continúa una y otra vez y cuando la consola imprime 'Hoy es domingo' la variable dia es ahora igual a 7 y el bucle while deja de ejecutarse.-->

---

# Ciclos anidados (Doble For)
Se habla de bucles anidados cuando un bucle se encuentra en el bloque de instrucciones de otro bloque.

Es posible anidar los <kbd>for</kbd>, es decir, meter uno dentro de otro. Esto puede ser muy útil si queremos iterar algún objeto que en cada elemento, tiene a su vez otra clase iterable. Podemos tener por ejemplo, una lista de listas, una especie de matriz.

<div grid="~ cols-2 gap-2" m="-t-2">

```python
lista = [[56, 34, 1],
         [12, 4, 5],
         [9, 4, 3]]
```

```python
for i in lista:
    print(i)
#[56, 34, 1]
#[12, 4, 5]
#[9, 4, 3]
```

</div>

```python
for i in lista:
    for j in i:
        print(j)
# Salida: 56,34,1,12,4,5,9,4,3
```

<!-- Si iteramos usando sólo un <kbd>for</kbd>, estaremos realmente accediendo a la segunda lista, pero no a los elementos individuales. -->

---

# Listas
Una <kbd>lista</kbd> es una estructura de datos y un tipo de dato en Python con características especiales. Lo especial de las listas en Python es que nos permiten almacenar cualquier tipo de valor como enteros, cadenas y hasta otras funciones.

## Métodos

<br>
<div grid="~ cols-3 gap-2" m="-t-2">

### append()

### count()

### index()

Añade un ítem al final de la lista.

Cuenta el número de veces que aparece un ítem.

Devuelve el índice en el que aparece un ítem (error si no aparece).

```python {1-3|4}
lista = [1,2,3,4,5]
lista.append(6)
lista
# [1, 2, 3, 4, 5, 6]
```

```python {1|2}
["Hola", "mundo", "mundo"].count("Hola")
# 1
```

```python {1|2}
["Hola", "mundo", "mundo"].index("mundo")
# 1
```
</div>

Documentación: [Ciclos anidados](https://docs.python.org/es/3/tutorial/datastructures.html), [Métodos de las listas](https://docs.hektorprofe.net/python/metodos-de-las-colecciones/metodos-de-las-listas/)
---

# Métodos Listas

<div grid="~ cols-3 gap-2" m="-t-2">

### clear()

### extend()

### insert()

Vacía todos los ítems de una lista.

Une una lista a otra.

Agrega un ítem a la lista en un índice específico.

```python {1-2|3}
lista.clear()
lista
# []
```

```python {1-4|5}
l1 = [1,2,3]
l2 = [4,5,6]
l1.extend(l2)
l1
# [1, 2, 3, 4, 5, 6]
```

```python {1-4|5|7-11|12}
# Primera posición (0)
l = [1,2,3]
l.insert(0,0)
l
# [0, 1, 2, 3]

# Última posición con len()
l = [5,10,15,25]
n = len(l)
l.insert(n,30)
l
# [5, 10, 15, 20, 25, 30]
```
</div>

---

# Métodos listas

<div grid="~ cols-3 gap-2" m="-t-2">

### pop()

### remove()

### reverse()

Extrae un ítem de la lista y lo borra.

Borra el primer ítem de la lista cuyo valor concuerde con el que indicamos.

Le da la vuelta a la lista actual.

```python {1-3|4-5}
l = [10,20,30,40,50]
print(l.pop())
print(l)
# 50
# [10, 20, 30, 40]
```

```python {1-4|4}
l = [20,30,30,30,40]
l.remove(30)
print(l)
# [20, 30, 30, 40]
```

```python {1-2|3}
l.reverse()
print(l)
# [40, 30, 30, 20]
```
</div>

<!-- Podemos indicarle un índice con el elemento a sacar (0 es el primer ítem)
```python
print(l.pop(0))
print(l)
# 10
# [20, 30, 40]
```

Las cadenas no tienen el método .reverse() pero podemos simularlo haciendo unas conversiones
```python
lista = list("Hola mundo")
lista.reverse()
cadena = "".join(lista)
cadena
# 'odnum aloH'    
``` -->

---

# Métodos listas

<div grid="~ cols-3 gap-2" m="-t-2">

### sort()

### split()

### join()

Ordena automáticamente los ítems de una lista por su valor de menor a mayor.




<!--
Podemos utilizar el argumento reverse=True para indicar que la ordene del revés.
```python
lista.sort(reverse=True)
lista
```
-->
</div>
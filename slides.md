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
10. Continúa una y otra vez y cuando la consola imprime 'Hoy es domingo' la variable dia es ahora igual a 7 y el bucle while deja de ejecutarse.
-->

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
# [56, 34, 1]
# [12, 4, 5]
# [9, 4, 3]
```

</div>

```python
for i in lista:
    for j in i:
        print(j)
# Salida: 56,34,1,12,4,5,9,4,3
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

<!-- 
Si iteramos usando sólo un <kbd>for</kbd>, estaremos realmente accediendo a la segunda lista, pero no a los elementos individuales. 
-->

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

Separa una cadena y coloca los elementos separados en una lista.

Formará una cadena de caracteres, con los elementos de una lista. Los elementos se guardarán en la cadena, separados por el caracter que especifiquemos.

```python {1-3|4}
lista = [5,-10,35,0,-65,100]
lista.sort()
lista
# [-65, -10, 0, 5, 35, 100]
```

```python {1-3|4}
cadena = "Mercurio, Venus, Tierra, Marte"
lista_planetas = cadena.split(',')
print (lista_planetas)
# ['Mercurio', ' Venus', ' Tierra', ' Marte']
```

```python {1-2|3}
so = ['windows','linux','mac']
print(",".join(so))
# windows,linux,mac
```
</div>

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

<!--
Podemos utilizar el argumento reverse=True para indicar que la ordene del revés.
```python
lista.sort(reverse=True)
lista
```
-->

---

# Ejemplo listas [1]
Escriba un programa que encuentre los números divisibles por 7 entre 2000 y 3200 (inclusive). Los números obtenidos serán impresos en una sola línea, separados por comas.

```python {all|1|2|3|4|5|all}
lista = [] # Primero creamos una lista vacía. Ésta lista contendrá los números divisibles por 7.
for i in range(2000, 3201): # Como se nos dió un rango (entre 2000 y 3200), escribimos la función range de 2000 a 3201.
    if (i%7==0):  # Comparamos si cada valor es múltiplo de 7 (si al dividirlo por 7 su residuo es 0)
        lista.append(str(i)) # Convertimos a cadena el valor, y lo agregamos al final de la lista.
print(','.join(lista)) # Convertimos toda la lista a cadena separando los elementos por comas.
```

```bash
2002, 2009, 2016, 2023, 2030, 2037, 2044, 2051, 2058, 2065, 2072, 2079, 2086, 2093, 2100, 2107,
2114, 2121, 2128, 2135, 2142, 2149, 2156, 2163, 2170, 2177, 2184, 2191, 2198, 2205, 2212, 2219, 2226,
2233, 2240, 2247, 2254, 2261, 2268, 2275, 2282, 2289, 2296, 2303, 2310, 2317, 2324, 2331, 2338, 2345,
2352, 2359, 2366, 2373, 2380, 2387, 2394, 2401, 2408, 2415, 2422, 2429, 2436, 2443, 2450, 2457, 2464,
2471, 2478, 2485, 2492, 2499, 2506, 2513, 2520, 2527, 2534, 2541, 2548, 2555, 2562, 2569, 2576, 2583, 2590,
2597, 2604, 2611, 2618, 2625, 2632, 2639, 2646, 2653, 2660, 2667, 2674, 2681, 2688, 2695, 2702,
2709, 2716, 2723, 2730, 2737, 2744, 2751, 2758, 2765, 2772, 2779, 2786, 2793, 2800, 2807, 2814,
2821, 2828, 2835, 2842, 2849, 2856, 2863, 2870, 2877, 2884, 2891, 2898, 2905, 2912, 2919, 2926,
2933, 2940, 2947, 2954, 2961, 2968, 2975, 2982, 2989, 2996, 3003, 3010, 3017, 3024, 3031, 3038,
3045, 3052, 3059, 3066, 3073, 3080, 3087, 3094, 3101, 3108, 3115, 3122, 3129, 3136, 3143, 3150,
3157, 3164, 3171, 3178, 3185, 3192, 3199
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

# Ejemplos listas [2]
Escriba un programa que acepte una secuencia de palabras separados por comas. Si la entrada suministrada al programa es la siguiente: saludos,hola,amigos,adios, la salida será: adios,amigos,hola,saludos. (Son las mismas palabras ordenadas alfabéticamente).

```python {all|1|2|3|4|all}
palabras = input("Escriba palabras separadas por comas: ") # Mostramos un mensaje al usuario y esperamos que escriba las palabras, éstas se guardan en la variable palabras.
lista = palabras.split(',') # La variable palabras es separada en varias cadenas considerando la coma como caracter de separación. Las palabras se guardan en una lista.
lista.sort() # La lista de palabras es ordenada alfabéticamente.
print(",".join(lista)) # La lista ordenada es nuevamente convertida a una cadena de caracteres separando cada elemento con una coma.
```

<br>

```bash
Escriba palabras separadas por comas: hola,chao,como estas
chao,como estas,hola
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

# Numpy
Es una librería de Python especializada en el cálculo numérico y el análisis de datos, especialmente para un gran volumen de datos. Son similares a las listas normales en Python, pero tienen la ventaja de ser más rápidas y tener más métodos integrados.

### Creación de arrays
- <kbd>np.array(lista)</kbd>: Crea un array a partir de la lista o tupla lista y devuelve una referencia a él.

<br>

<div grid="~ cols-3 gap-2" m="-t-2">

  ```python {1-3|4}
  # Array de una dimensión
  a1 = np.array([1, 2, 3])
  print(a1)
  # [1 2 3]
  ```

  ```python {1-3|4-5}
  # Array de dos dimensiones
  a2 = np.array([[1, 2, 3], [4, 5, 6]])
  print(a2)
  # [[1 2 3]
  # [4 5 6]]
  ```

  ```python {1-3|4-8}
  # Array de tres dimensiones
  a3 = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])
  print(a3)
  # [[[ 1  2  3]
  # [ 4  5  6]]

  # [[ 7  8  9]
  # [10 11 12]]]
  ```

</div>

Para más información: [Manual Numpy](https://aprendeconalf.es/docencia/python/manual/numpy/), [Guía sencilla Numpy](https://pharos.sh/tutorial-de-numpy-una-guia-sencilla-basada-en-ejemplos/), [Paquete Numpy](https://www.freecodecamp.org/espanol/news/la-guia-definitiva-del-paquete-numpy-para-computacion-cientifica-en-python/)

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

# Creación de arrays

- <kbd>np.empty(dimensiones)</kbd>: Crea y devuelve una referencia a un **array vacío** con las dimensiones especificadas en la tupla dimensiones.
- <kbd>np.zeros(dimensiones)</kbd>: Crea y devuelve una referencia a un array con las dimensiones especificadas en la tupla dimensiones cuyos elementos son **todos ceros**.
- <kbd>np.ones(dimensiones)</kbd>: Crea y devuelve una referencia a un array con las dimensiones especificadas en la tupla dimensiones cuyos elementos son **todos unos**.
- <kbd>np.full(dimensiones, valor)</kbd>: Crea y devuelve una referencia a un array con las dimensiones especificadas en la tupla dimensiones cuyos elementos son **todos valor**.
- <kbd>np.arange(inicio, fin, salto)</kbd>: Crea y devuelve una referencia a un array de una dimensión cuyos elementos son la secuencia desde inicio hasta fin tomando valores cada salto.
- <kbd>np.linspace(inicio, fin, n)</kbd>: Crea y devuelve una referencia a un array de una dimensión cuyos elementos son la secuencia de **n valores equidistantes** desde inicio hasta fin.
- <kbd>np.random.random(dimensiones)</kbd>: Crea y devuelve una referencia a un array con las dimensiones especificadas en la tupla dimensiones cuyos elementos son **aleatorios**.

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

<!--Una tupla es una colección de datos cuyo orden es inalterable, o sea, son elementos ordenados en una secuencia específica y que posee importancia. En Python, los tuples se escriben entre paréntesis.

```python
print(np.zeros(3,2))
# [[0. 0. 0.]
# [0. 0. 0.]]
print(np.arange(1, 10, 2))
# [1 3 5 7 9]
print(np.linspace(0, 10, 5))
# [ 0.   2.5  5.   7.5 10. ]
``` -->

---

# Acceder a los elementos de un array
Para acceder a los elementos contenidos en un array se usan índices al igual que para acceder a los elementos de una lista, pero indicando los índices de cada dimensión separados por comas.

Al igual que para listas, los índices de cada dimensión comienzan en 0.

También es posible obtener subarrays con el operador dos puntos : indicando el índice inicial y el siguiente al final para cada dimensión, de nuevo separados por comas.

```python {1-2|3|5|6|8|9-10}
a = np.array([[1, 2, 3], [4, 5, 6]])
print(a[1, 0])  # Acceso al elemento de la fila 1 columna 0
# 4

print(a[1][0])  # Otra forma de acceder al mismo elemento
# 4

print(a[:, 0:2])
# [[1 2]
# [4 5]]
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

# Otros métodos Numpy

## Remodelación de matrices
Usando NumPy puedes convertir una matriz unidimensional en una matriz bidimensional usando el <kbd>reshape</kbd> método.

```python {1|2|3}
nums = np.arange(1, 17) # Creamos una matriz de 16 elementos - unidimensional
nums2 = nums.reshape(4, 4) # Vamos a convertirlo en una matriz bidimensional de 4 filas y 4 columnas
# array([[ 1,  2,  3,  4],
#       [ 5,  6,  7,  8],
#       [ 9, 10, 11, 12],
#       [13, 14, 15, 16]])
```

_Es pertinente mencionar que no puede remodelar una matriz si el número de elementos en la matriz unidimensional no es igual al producto de filas y columnas de la matriz remodelada._

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

# Otros métodos Numpy

## Split [^1]
Permite dividir una matriz en varias submatrices.

```python {1-2|3}
x = np.arange(9.0)
np.split(x, 3)
# [array([0.,  1.,  2.]), array([3.,  4.,  5.]), array([6.,  7.,  8.])]
```
<br>

<div grid="~ cols-3 gap-2" m="-t-2">

```python {1-3|4-6}
# Crear una matriz de 3 fil, 4 col
A = np.arange(12).reshape((3, 4))
print(A)
# array([[ 0,  1,  2,  3],
#    [ 4,  5,  6,  7],
#    [ 8,  9, 10, 11]])
```

```python {1-2|3-7}
# División vertical
print(np.split(A, 2, axis=1))
# [array([[0, 1],
#        [4, 5],
#        [8, 9]]), array([[ 2,  3],
#        [ 6,  7],
#        [10, 11]])]
```

```python {1-2|3}
# División horizontal
print(np.split(A, 3, axis=0))
# [array([[0, 1, 2, 3]]), array([[4, 5, 6, 7]]), array([[ 8,  9, 10, 11]])]
```
</div>

[^1]: [Numpy array split](https://programmerclick.com/article/5547696995/)

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

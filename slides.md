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
lineNumbers: true
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
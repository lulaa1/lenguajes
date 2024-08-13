# Lenguajes funcionales:
- Los lenguajes funcionales son un tipo de lenguaje de programación que se basa en el paradigma de la programación funcional, se enfoca en la ejecución de secuencias de instrucciones, como en la programación imperativa, los lenguajes funcionales se centran en la evaluación de funciones matemáticas y en el uso de expresiones para describir el comportamiento del programa.
### Caracteristicas de los Lenguajes Funcionales:
- **Funciones como Valores**:  las funciones pueden ser asignadas a variables, pasadas como argumentos a otras funciones y retornadas como resultados de otras funciones. Esto permite una gran flexibilidad en el diseño del software.
~~~
let cuadrado x = x * x
let doble x = 2 * x
let resultado = doble (cuadrado 5)  -- Resultado es 50
~~~
- **Inmutabilidad:** En los lenguajes funcionales vienen a ser inmutables, es decir, una vez que se crea una estructura de datos, ya no se puede modificar. En lo contrario se crean nuevas estructuras a partir de las existentes.
 ~~~
let lista = [1, 2, 3]
let nuevaLista = 0 : lista  -- nuevaLista es [0, 1, 2, 3]
~~~~
- **Funciones puras:**  son aquellas que, dado un mismo conjunto de entradas, siempre se producirán el mismo conjunto de salidas y no tendrán efectos secundarios observables (como modificar una variable global o escribir en un archivo).
~~~
suma :: Int -> Int -> Int
suma x y = x + y 
~~~
- **Evaluación Perezosa (Lazy Evaluation):** En algunos lenguajes funcionales utilizan evaluación perezosa, para que las expresiones no se evalúen hasta que se necesiten. Esto puede mejorar la eficiencia y permitir el uso de estructuras de datos infinitas.
~~~
let infinita = [1..]  -- Lista infinita de números naturales
let primeros10 = take 10 infinita  -- Toma los primeros 10 elementos
~~~
- **Composición de Funciones:** La composición de funciones se permite construir nuevas funciones combinando las funciones existentes. Esto es útil para crear funciones más complejas a partir de funciones más simples.
~~~
let sumaYMultiplica x y z = (x + y) * z
let incrementa = (+1)
let doble = (*2)
let incrementaYMultiplica = sumaYMultiplica `on` incrementa
~~~
- **Recursion:** La recursión es una técnica fundamental en la programación funcional. Es debido a la falta de bucles imperativos, tambien en los lenguajes funcionales a menudo se definen en términos de sí mismas para realizar iteraciones
~~~
factorial :: Int -> Int
factorial 0 = 1
factorial n = n * factorial (n - 1)
~~~



 

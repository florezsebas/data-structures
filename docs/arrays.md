# Arreglos
## Introduccion a los arreglos
Los arrays, también conocidos como arreglos, son estructuras de datos fundamentales en la programación. Representan una colección ordenada de elementos del mismo tipo. Cada elemento en un array se almacena en una posición específica, llamada índice. El índice se utiliza para acceder y manipular los elementos individuales dentro del array.

![array_image](/images/arrays/array.svg)

Los arrays son estáticos en su tamaño, lo que significa que se les asigna un espacio de memoria fijo durante su creación y no pueden crecer o reducirse dinámicamente. La capacidad de almacenamiento de un array se define al momento de su declaración y no puede cambiarse posteriormente.

En la mayoría de los lenguajes de programación, los índices de los arrays comienzan en cero, lo que significa que el primer elemento se accede utilizando el índice 0. Por ejemplo, en un array de tamaño n, el primer elemento se encuentra en el índice 0 y el último elemento se encuentra en el índice n-1.

Los arrays ofrecen varias ventajas, como un acceso rápido a los elementos mediante el uso de índices, una representación ordenada de los datos y la capacidad de realizar operaciones eficientes como la búsqueda y el ordenamiento.

Es importante tener en cuenta que los arrays suelen tener un tamaño fijo y contiguo en la memoria, lo que significa que suelen requerir un espacio de memoria continuo para almacenar todos los elementos. Esta limitación puede tener implicaciones en términos de uso eficiente de la memoria y la capacidad de manejar grandes cantidades de datos.

## Operaciones básicas de arrays

### Inserción en un array
La inserción en un array implica agregar un nuevo elemento en una posición específica. Puede ser al principio, al final o en cualquier posición intermedia del array. Dependiendo del lenguaje de programación, puedes utilizar el índice para indicar la posición de inserción. Si el array está lleno, es posible que necesites redimensionarlo para dar cabida al nuevo elemento. Algunos lenguajes de programación proporcionan métodos o funciones específicas para insertar elementos en un array.

### Eliminación de un elemento en un array
La eliminación implica eliminar un elemento existente en el array. Puedes especificar la posición del elemento que deseas eliminar utilizando el índice correspondiente. Después de eliminar un elemento, es posible que debas reorganizar el array para asegurarte de que no haya espacios vacíos entre los elementos restantes. Al igual que en la inserción, algunos lenguajes de programación tienen métodos o funciones específicas para eliminar elementos de un array.

### Búsqueda de un elemento en un array
La búsqueda implica encontrar la posición de un elemento específico dentro del array. Puedes recorrer el array iterativamente, comparando cada elemento con el valor buscado hasta encontrar una coincidencia. Si encuentras el elemento, puedes devolver su posición (índice). Si el elemento no está presente, puedes devolver un valor especial, como -1, para indicar que no se encontró. Algunos lenguajes de programación proporcionan funciones integradas para realizar búsquedas en un array.

## Buscar en un Array
### Busqueda Lineal
La búsqueda lineal es un algoritmo de búsqueda utilizado para encontrar un elemento específico en una lista de elementos. Consiste en examinar secuencialmente cada elemento de la lista hasta encontrar el elemento buscado o hasta recorrer toda la lista sin encontrarlo.

#### Algoritmo
1. Iniciar en el primer elemento de la lista.
2. Comparar el elemento actual con el elemento buscado.
3. Si el elemento actual es igual al elemento buscado, se ha encontrado el elemento y se puede finalizar la búsqueda.
4. Si el elemento actual no es igual al elemento buscado, avanzar al siguiente elemento de la lista.
5. Si se ha alcanzado el final de la lista y no se ha encontrado el elemento buscado, significa que el elemento no está presente en la lista.

### Busqueda Binaria
La búsqueda binaria es un algoritmo de búsqueda utilizado para encontrar rápidamente un elemento en una lista ordenada. A diferencia de la búsqueda lineal, que examina secuencialmente cada elemento, la búsqueda binaria divide repetidamente a la mitad el espacio de búsqueda hasta encontrar el elemento deseado.

#### Algoritmo
1. Iniciar definiendo los límites del espacio de búsqueda. El límite inferior será el primer índice de la lista, y el límite superior será el último índice de la lista.
2. Calcular el punto medio del espacio de búsqueda, redondeando hacia abajo si es necesario. Este punto medio se obtiene sumando el límite inferior y el límite superior, y dividiendo el resultado por 2.
3. Comparar el elemento en el punto medio con el elemento buscado.
4. Si el elemento en el punto medio es igual al elemento buscado, se ha encontrado el elemento y se puede finalizar la búsqueda.
5. Si el elemento en el punto medio es mayor que el elemento buscado, se reajusta el límite superior para que sea el punto medio menos uno, y se vuelve al paso 2.
6. Si el elemento en el punto medio es menor que el elemento buscado, se reajusta el límite inferior para que sea el punto medio más uno, y se vuelve al paso 2.
7. Repetir los pasos 2 a 6 hasta que se encuentre el elemento buscado o hasta que el límite inferior sea mayor que el límite superior.
Si se ha recorrido todo el espacio de búsqueda y no se ha encontrado el elemento, significa que el elemento no está presente en la lista.

## Ordenamiento de arrays
### Selection Sort (Seleccion)
El enfoque del algoritmo de selección (selection sort) es ordenar una lista de elementos, ya sea en forma ascendente o descendente, seleccionando repetidamente el elemento más pequeño (o más grande) de la lista y colocándolo en la posición correcta.

#### Algoritmo
1. Iniciar con un array desordenado.
2. Iterar a través del array desde el inicio hasta el penúltimo elemento (índices 0 a n-2):
    1. Suponer que el elemento actual es el más pequeño.
    2. Iterar a través de los elementos restantes (índices i+1 a n-1):
    3. Si se encuentra un elemento más pequeño, actualizar el índice del elemento más pequeño.
    4. Intercambiar el elemento actual con el elemento más pequeño encontrado en la iteración interna.
3. El array se considera ordenado cuando se haya realizado el paso anterior para todos los elementos del array.

### Insertion Sort (Insercion)
El algoritmo de ordenación Insertion Sort (ordenamiento por inserción) es un algoritmo simple y eficiente que ordena una lista de elementos comparando y moviendo elementos adyacentes hasta que la lista esté completamente ordenada. El enfoque de este algoritmo es similar a cómo ordenaríamos una baraja de cartas en la vida real.

#### Algoritmo
1. Comienza con la lista de elementos desordenados.
2. El primer elemento de la lista se considera una sublista ordenada de un solo elemento.
3. Toma el siguiente elemento de la lista desordenada y compáralo con los elementos en la sublista ordenada.
4. Desplaza todos los elementos en la sublista ordenada que sean mayores que el elemento actual una posición hacia la derecha.
5. Inserta el elemento actual en la posición vacía dejada por el desplazamiento.
6. Repite los pasos 3 a 5 hasta que todos los elementos hayan sido considerados.
7. Al finalizar, la lista estará completamente ordenada.

### Bubble Sort (Burbuja)
El enfoque del Bubble Sort es comparar repetidamente pares adyacentes de elementos en una lista y, si están en el orden incorrecto, intercambiarlos. El proceso se repite hasta que la lista esté completamente ordenada.

#### Algoritmo
1. Comenzar con una lista de elementos a ordenar.
2. Comparar el primer elemento con el siguiente elemento de la lista.
3. Si el primer elemento es mayor que el segundo elemento, intercambiarlos.
4. Mover al siguiente par de elementos y repetir el proceso de comparación e intercambio.
6. Continuar realizando comparaciones e intercambios hasta llegar al final de la lista.
7. Al llegar al final de la lista, el elemento más grande estará en su posición final.
8. Repetir los pasos 2 al 6 para todos los elementos restantes de la lista, excepto los ya colocados en su posición final.
9. Repetir los pasos 2 al 7 hasta que la lista esté completamente ordenada.

## Matrices
En programación, una matriz es una estructura de datos que almacena elementos en una cuadrícula de dos o más dimensiones. También se le conoce como un array multidimensional. A diferencia de los arrays unidimensionales (vectores), que tienen una sola fila o columna de elementos, las matrices tienen filas y columnas, formando una especie de tabla o rejilla.

Cada elemento en una matriz se identifica mediante su posición en la estructura. Las filas y las columnas están indexadas numéricamente, comenzando generalmente desde cero. Por ejemplo, en una matriz de 3x3, se puede acceder a un elemento utilizando dos índices: uno para la fila y otro para la columna.

Las matrices son muy útiles para almacenar y manipular datos estructurados. Pueden contener diferentes tipos de elementos, como números, caracteres, objetos u otros arrays. Las matrices se utilizan en una amplia variedad de aplicaciones, desde la representación de imágenes y sonidos hasta la resolución de problemas matemáticos y científicos complejos

## Arrays Dispersos (Matrix Dispersa)
Los arrays dispersos, también conocidos como matrices dispersas, son estructuras de datos que se utilizan para representar matrices en las que la mayoría de los elementos tienen un valor predeterminado o nulo. En contraste con los arrays densos, que almacenan todos los elementos de una matriz, los arrays dispersos solo almacenan los elementos distintos de cero o del valor predeterminado.

Esto es especialmente útil cuando se trabaja con matrices grandes que tienen una gran cantidad de elementos que son iguales a cero o a un valor común. En lugar de asignar memoria y almacenar estos elementos repetitivos, los arrays dispersos solo almacenan los elementos distintos de cero, junto con su ubicación en la matriz.Los arrays dispersos, también conocidos como matrices dispersas, son estructuras de datos que se utilizan para representar matrices en las que la mayoría de los elementos tienen un valor predeterminado o nulo. En contraste con los arrays densos, que almacenan todos los elementos de una matriz, los arrays dispersos solo almacenan los elementos distintos de cero o del valor predeterminado.

Esto es especialmente útil cuando se trabaja con matrices grandes que tienen una gran cantidad de elementos que son iguales a cero o a un valor común. En lugar de asignar memoria y almacenar estos elementos repetitivos, los arrays dispersos solo almacenan los elementos distintos de cero, junto con su ubicación en la matriz.
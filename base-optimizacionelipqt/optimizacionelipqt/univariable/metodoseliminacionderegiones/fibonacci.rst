.. _fibonacci:

Método de Búsqueda de Fibonacci
===========================================================================

Este archivo documenta el método de búsqueda de Fibonacci para encontrar un intervalo [a, b] que contiene un mínimo local de una función dada.

Fibonacci
--------------------------------

Función para calcular el (n+1)-ésimo número de Fibonacci.

Parámetros
~~~~~~~~~~~

- `n` (int): La función objetivo que se desea minimizar.

Retorno
~~~~~~~~~~~

La función retorna el (n+1)-ésimo número de Fibonacci.

Método de Búsqueda de Fibonacci
--------------------------------

La función `fibonacci_search` implementa un método iterativo basado en la secuencia de Fibonacci para buscar un intervalo [a, b] que contenga un mínimo local de la función objetivo. Se utiliza un número dado de iteraciones para ajustar el tamaño del intervalo en cada paso.

Parámetros
~~~~~~~~~~~

- `funcion` (callable): La función objetivo que se desea minimizar.
- `a` (float): Límite inferior del intervalo inicial.
- `b` (float): Límite superior del intervalo inicial.
- `n` (int): Número de iteraciones, relacionado con la precisión del método.

Retorno
~~~~~~~~~~~

La función retorna un tuple (a, b) que representa el intervalo [a, b] que contiene un mínimo local de la función. Los límites a y b se actualizan iterativamente según el método de búsqueda de Fibonacci.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python
    
    import numpy as np
    import paqueteoptimizacionelizabethrm as op 

    p14 = op.univariable.metodoseliminacionderegiones.fibonacci_search(op.funciones.funcion_4, -1.5, 3, 20)
    print("Algoritmo Fibonacci Función 4", p14)

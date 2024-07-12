.. _exhaustiva:

Método de Búsqueda Exhaustiva
======================================================================

El método de búsqueda exhaustiva es el más simple de todos, y consiste en calcular los valores de la función en varios puntos igualmente espaciados para enmarcar el óptimo. La búsqueda inicia desde un límite inferior y se comparan tres valores consecutivos de la función, asumiendo que esta es unimodal. Dependiendo del resultado de la comparación, se puede terminar la búsqueda o continuar reemplazando uno de los puntos por uno nuevo. Este proceso se repite hasta que se logra enmarcar el mínimo.

Método de Búsqueda Exhaustiva
------------------------------

La función `exhaustive_search_method` implementa un algoritmo de búsqueda exhaustiva para encontrar un intervalo [x1, x3] donde una función tiene un mínimo local. Se basa en una precisión dada para determinar el tamaño del paso en la búsqueda.

Parámetros
~~~~~~~~~~~

- `a` (float): Límite inferior del intervalo de búsqueda.
- `b` (float): Límite superior del intervalo de búsqueda.
- `precision` (float): Tamaño del paso para la búsqueda.
- `funcion` (callable): La función que se busca minimizar.

Retorno
~~~~~~~~~~~

La función retorna un tuple (x1, x3) que representa el intervalo [x1, x3] que contiene un mínimo local de la función. Si no se encuentra tal intervalo, devuelve None.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python
    
    import numpy as np
    import paqueteoptimizacionelizabethrm as op 

    p13 = op.univariable.metodoseliminacionderegiones.exhaustiva.exhaustive_search_method(-1.5, 3, 0.001, op.funciones.funcion_4)
    print("Algoritmo Exhaustiva Funcion 4", p13)

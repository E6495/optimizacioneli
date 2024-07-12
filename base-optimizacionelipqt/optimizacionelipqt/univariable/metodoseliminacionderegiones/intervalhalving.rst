.. _intervalhalving:

Método de Interval Halving Method
===========================================================

En el método de división del intervalo, se consideran los valores de la función en tres puntos equidistantes dentro del intervalo (a,b). Estos puntos dividen el espacio de búsqueda en cuatro regiones, y se usa una regla de eliminación para descartar parte del espacio basado en los valores de la función. Dependiendo de las comparaciones, se puede reducir el intervalo a la mitad o en un 25%, y este proceso se repite hasta encontrar un intervalo suficientemente pequeño. El método se llama de división del intervalo porque en cada iteración se conserva exactamente la mitad del espacio de búsqueda.

Método de Bisección
--------------------------

La función `interval_halving_method` implementa el método de Interval halving Method, que divide iterativamente un intervalo [a, b] en la mitad y decide en cuál mitad buscar el mínimo local de la función objetivo. La función itera hasta que la longitud del intervalo sea menor que una tolerancia `epsilon`.

Parámetros
~~~~~~~~~~~

- `a` (float): Límite inferior del intervalo inicial.
- `b` (float): Límite superior del intervalo inicial.
- `funcion` (callable): La función objetivo a minimizar.
- `epsilon` (float): La tolerancia para la longitud del intervalo.

Retorno
~~~~~~~~~~~

La función retorna un tuple que representa el intervalo [a, b] que contiene un mínimo local de la función.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python
    
    import numpy as np
    import paqueteoptimizacionelizabethrm as op 

    p16 = op.univariable.metodoseliminacionderegiones.intervalhalving.interval_halving_method(-5, 5, op.funciones.funcion_3, 0.0001)
    print("Funcion 2 Interval", p16)

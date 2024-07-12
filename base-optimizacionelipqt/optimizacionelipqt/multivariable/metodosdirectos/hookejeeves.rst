.. _optimizacioneli-multivariable-hooke_jeeves:

Método de Hooke-Jeeves
=======================

El método de Hooke-Jeeves es un algoritmo de optimización heurístico que utiliza un enfoque de búsqueda directa y patrones para encontrar el mínimo de una función. Consiste en realizar movimientos exploratorios para encontrar el mejor punto en la vecindad del punto actual, seguidos de movimientos de patrón que combinan puntos para avanzar hacia una mejor solución. 

Función de movimiento exploratorio
--------------------

El punto actual se perturba en direcciones positivas y negativas a lo largo de cada variable, una a la vez, y se registra el mejor punto. El punto actual se cambia al mejor punto al final de cada perturbación de variable.

Parámetros
~~~~~~~~~~~
- ``xc`` (array-like): Punto actual en el espacio de búsqueda.
- ``delta`` (array-like): Vector de pasos para moverse en cada dirección.
- ``function`` (callable): Función objetivo a minimizar.

Retorna
~~~~~~~~~~~
- ``tuple``: Nuevo punto en el espacio de búsqueda, arreglo booleano indicando éxito de cada movimiento, punto anterior.

Función de movimiento de patrón
------------------

Un nuevo punto se encuentra al saltar desde el punto mejor actual en la dirección que conecta el punto mejor anterior con el punto base actual.

Parámetros
~~~~~~~~~~~
- ``x_current`` (array-like): Punto actual en el espacio de búsqueda.
- ``x_previous`` (array-like): Punto anterior en el espacio de búsqueda.

Retorna
~~~~~~~~~~~
- ``array-like``: Nuevo punto calculado según el movimiento de patrón.

Función de Hooke Jeeves
---------------------

Método Hooke Jeeves

Parámetros
~~~~~~~~~~~
- ``initial_point`` (array-like): Punto inicial de búsqueda.
- ``deltas`` (array-like): Vector de pasos para moverse en cada dirección.
- ``alpha`` (float): Factor de reducción de pasos en caso de fracaso en la búsqueda.
- ``epsilon`` (float): Tolerancia para detener el algoritmo.
- ``function`` (callable): Función objetivo a minimizar.

Retorna
~~~~~~~~~~~
- ``tuple``: Punto óptimo encontrado que minimiza la función, número de iteraciones realizadas.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python

   import numpy as np 
   import paqueteoptimizacionelizabethrm as op 

   p2, iterations = op.multivariable.metodosdirectos.hookejeeves.hooke_jeeves([1, 2], [0.1, 0.1], 1.5, 0.001, lambda *args: op.funciones.himmelblau_function(list(args))
   print("Algoritmo Hooke Jeeves Función Himmelblau:", p2, iterations)
)
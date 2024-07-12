.. _optimizacioneli-multivariable-tweak:

Método de Recocido Simulado
==================================

El algoritmo varía de Hill-Climbing en su decisión de cuándo reemplazar X, la solución candidata original, con U, su hijo recién modificado. Específicamente: si U es mejor que X, se reemplaza X por U como de costumbre. Pero si U es peor que X, aún se puede reemplazar X con U con cierta probabilidad

Función tweak
-------------------

Función que aplica una pequeña pertubación aleatoria a una matriz dada.

Parámetros
~~~~~~~~~~~
- ``X`` (numpy array): Matriz de entrada a la cual se le aplicará la perturbación.

Retorna
~~~~~~~~~~~
- ``numpy array``: Matriz perturbada con valores aleatorios uniformemente distribuidos dentro del rango [-0.5, 0.5].


Algoritmo de Recocido Simulado
-------------------

Implementación del algoritmo de Recocido Simulado para optimización.

Parámetros
~~~~~~~~~~~
- ``f`` (function): Función objetivo a minimizar.
- ``x0`` (list or numpy array): Punto inicial de la búsqueda.
- ``alpha`` (float): Factor de enfriamiento para la temperatura.
- ``T_initial`` (float): Temperatura inicial.
- ``T_min`` (float): Temperatura mínima en la que se detiene la búsqueda.
- ``metropolis_size`` (int): Número de iteraciones por cada temperatura.

Retorna
~~~~~~~~~~~
- ``numpy array``: El mejor punto encontrado que minimiza la función ``f``.
- ``list``: Historial de puntos explorados durante la búsqueda.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python

   import numpy as np
   import paqueteoptimizacionelizabethrm as op 

   p5, h2 = op.multivariable.metodosdirectos.recocido.simulated_annealing(op.funciones.sphere_function, [1, 2], 0.9, 10, 0.1, 1000)
   print("Algoritmo Recocido Función Sphere", p5)

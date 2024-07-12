.. _optimizacioneli-multivariable-random_walk:

Algoritmo de Colina
=========================

El algoritmo de Colina es una técnica de optimización que genera pasos aleatorios para explorar el espacio de búsqueda en busca de un mínimo global. Se generan soluciones aleatorias a partir de un punto dado, pero solo se cambia de posición sí y sólo sí, la nueva solución es mejor.


Función generación random
--------------

Genera un paso aleatorio para la optimización.

Parámetros
~~~~~~~~~~~
- ``x`` (array-like): Punto actual en el espacio de búsqueda.
- ``sigma`` (float): Desviación estándar para la distribución normal que genera el paso aleatorio.

Retorna
~~~~~~~~~~~
- ``np.ndarray``: Nuevo punto generado como un paso aleatorio desde x.

Función colina
----------

Algoritmo de Random Walk Colina para la optimización.

Parámetros
~~~~~~~~~~~
- ``f`` (callable): Función objetivo a minimizar.
- ``terminate`` (callable): Función de terminación que determina cuándo detener el algoritmo.
- ``max_iter`` (int): Número máximo de iteraciones permitidas.
- ``x0`` (array-like): Punto inicial de la búsqueda.
- ``sigma`` (float): Desviación estándar para generar pasos aleatorios.

Retorna
~~~~~~~~~~~
- ``tuple``: Mejor punto encontrado y lista de puntos históricos durante la búsqueda.

Función de terminación
----------

Criterio de terminación basado en el número máximo de iteraciones.

Parámetros
~~~~~~~~~~~
- ``max_iter`` (int): Número máximo de iteraciones permitidas.

Retorna
~~~~~~~~~~~
``callable``: Función que verifica si el número atual de iteraciones ha alcanzado max_iter.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python

   import numpy as np
   import paqueteoptimizacionelizabethrm as op 

   p1, h1 = op.multivariable.metodosdirectos.colina.random_walk_colina(op.funciones.sphere_function, op.multivariable.metodosdirectos.colina.max_iterations_terminate(1000), 1000, [2, 15], 0.9)
   print("Método Colina Función Sphere", p1)
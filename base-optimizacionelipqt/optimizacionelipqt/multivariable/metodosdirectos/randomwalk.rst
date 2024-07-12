.. _optimizacioneli-multivariable-random_walk:

Algoritmo Random Walk
=====================

El algoritmo Random Walk es una técnica estocástica que genera pasos aleatorios para explorar el espacio de búsqueda y encontrar soluciones óptimas.
No utiliza información extra del problema durante la búsqueda. Inicia en un lugar aleatorio y toma pasos aleatorios.

Función Random Walk
----------------

   Implementa el algoritmo Random Walk para minimizar una función objetivo.

   Parámetros
   ----------
   - ``f`` (callable): Función objetivo a minimizar.
   - ``x0`` (list or numpy array): Punto de inicio del algoritmo.
   - ``max_iter`` (int): Número máximo de iteraciones.
   - ``mu`` (float): Media de la distribución normal para generar pasos aleatorios.
   - ``sigma`` (float): Desviación estándar de la distribución normal para generar pasos aleatorios.

   Retorna
   -------
   - ``numpy array``: La mejor solución encontrada que minimiza la función ``f``.
   - ``list``: Historial de puntos visitados durante la búsqueda.

   Ejemplo de Uso
   --------------

   .. code-block:: python

      import numpy as np
      import paqueteoptimizacionelizabethrm as op

      p4, h = op.multivariable.metodosdirectos.randomwalk.random_walk(op.funciones.himmelblau_function, [0, 2], 1000, 0.3, 0.8)
      print("Algoritmo Random Walk Función Himmelblau", p4)
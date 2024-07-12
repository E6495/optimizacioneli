.. _neldermeadsimplex:
.. _optimizacioneli-multivariable-mead_simplex:

Algoritmo de Mead (Nelder-Mead)
===============================

El algoritmo de Mead, también conocido como método Nelder-Mead, es un método de optimización sin restricciones que utiliza un simplex para encontrar el mínimo de una función. consiste en utilizar N+1 puntos en el simplex inicial para un problema de N variables y, en cada iteración, reemplazar el peor punto mediante una serie de operaciones de reflexión, expansión y contracción basadas en los valores de la función. Se calcula el centroide de todos los puntos excepto el peor, se refleja el peor punto respecto al centroide y, dependiendo del valor de la función en el punto reflejado, se puede realizar una expansión o una contracción. Este proceso se repite hasta alcanzar la convergencia.

Función Simplex
--------------

   Estructura del simplex inicial para el algoritmo de Mead (Nelder-Mead).

   Parámetros
   ----------
   - ``alpha`` (float): Parámetro de ajuste para calcular los puntos del simplex inicial.
   - ``punto_inicial`` (list): Punto inicial alrededor del cual se genera el simplex.

   Retorna
   -------
   - ``list``: Lista de puntos que conforman el simplex inicial.

Funcion Mead Simplex
--------------------

   Implementación del método de Mead (Nelder-Mead) para optimización sin restricciones.

   Parámetros
   ----------
   - ``funcion`` (callable): Función objetivo que se desea minimizar.
   - ``punto_inicial`` (list): Punto inicial alrededor del cual se realiza la búsqueda.
   - ``epsilon`` (float): Criterio de convergencia, diferencia mínima entre los valores de la función.
   - ``gamma`` (float): Parámetro de reflexión.
   - ``beta`` (float): Parámetro de contracción.

   Retorna
   -------
   - ``tuple``: Punto óptimo encontrado y lista de simplex en cada iteración.

   Ejemplo de Uso
   --------------

   .. code-block:: python

      import numpy as np
      import paqueteoptimizacionelizabethrm as op 

      p3, hsf = op.multivariable.metodosdirectos.neldermeadsimplex.mead_simplex(op.funciones.himmelblau_function, np.array([1.0, 2.0]), 0.00001, 2, 0.5)
      print("Algoritmo Mead Simplex Función Himmenblau", p3)
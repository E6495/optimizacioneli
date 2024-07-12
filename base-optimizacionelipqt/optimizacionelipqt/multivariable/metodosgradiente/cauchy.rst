.. _cauchy:

Método del Cauchy
================

Utiliza la dirección negativa del gradiente en cada punto xs. En cada iteración, se calcula el gradiente en el punto actual y se realiza una búsqueda unidimensional en la dirección negativa de este gradiente para encontrar el punto mínimo a lo largo de esa dirección. El algoritmo continúa iterativamente hasta encontrar un punto con un vector gradiente suficientemente pequeño, garantizando la mejora del valor de la función en cada iteración
Este método trabaja bien cuando x(0) se encuentra lejos del óptimo. Cuando el punto actual está muy cercano el cambio en el gradiente es pequeño. Esto hace que la convergencia se lenta, para acelerarla se puede usar las derivadas de segundo orden.

Implementación del Método de Cauchy
-----------------------------------

La función `Cauchy` permite varios métodos de búsqueda unidireccional para encontrar un tamaño de paso (`alpha`) adecuado durante cada iteración:

- **Búsqueda Fibonacci**: Utiliza el algoritmo de búsqueda Fibonacci para encontrar `alpha`.
- **Método de Cauchy-Raphson**: Utiliza el método de Cauchy-Raphson para encontrar `alpha`.
- **Búsqueda de la Sección Dorada**: Aplica la búsqueda de la sección dorada para determinar `alpha`.
- **Método de Intervalo de Mitad**: Implementa el método de intervalo de mitad para `alpha`.
- **Método de Fase de Limitación**: Utiliza el método de fase de limitación para encontrar `alpha`.
- **Método de Búsqueda Exhaustiva**: Aplica la búsqueda exhaustiva para determinar `alpha`.
- **Método de Bisección**: Implementa el método de bisección para encontrar `alpha`.
- **Método de Secante**: Utiliza el método de la secante para determinar `alpha`.

Función de Gradiente
-----------------------------------

Calcula el gradiente de una función en un punto dado utilizando aproximaciones numéricas de las derivadas parciales.

Parámetros
~~~~~~~~~~~
- ``f`` (callable): Función cuyo gradiente se busca calcular.
- ``x`` (array-like): Punto en el cual se evalúa el gradiente.
- ``deltaX`` (float, optional): Paso para la aproximación numérica de las derivadas parciales. Por defecto es 0.001.

Retorna
~~~~~~~~~~~
- ``list``: Gradiente de ``f`` en ``x``.

Función de Cauchy
-----------------------------------

Implementa el método de Cauchy para la optimización de funciones.

Parámetros
~~~~~~~~~~~
- ``funcion`` (callable): Función objetivo a minimizar.
- ``x0`` (array-like): Punto inicial de búsqueda.
- ``epsilon1`` (float): Tolerancia para la norma del gradiente que determina la convergencia.
- ``epsilon2`` (float): Tolerancia para la diferencia relativa entre dos iteraciones consecutivas.
- ``M`` (int): Número máximo de iteraciones permitidas.
- ``metodo`` (str): Método para la búsqueda de paso de línea ('biseccion', 'interval', 'bounding', 'secante', 'exhaustiva', 'dorado', 'fibonacci', 'newton').

Retorna
~~~~~~~~~~~
- ``array-like``: Punto óptimo encontrado que minimiza la función ``f``.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python

   import numpy as np
   import paqueteoptimizacionelizabethrm as op 

   p8 = op.multivariable.metodosgradiente.cauchy(op.funciones.himmelblau_function, np.array([0.1, 0.1]), 0.0001, 0.0001, 100, 'fibonacci')
   print("Algoritmo Cauchy Función Himmelblau", p8)

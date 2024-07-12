.. _graficas:

Gráficas 2D de Funciones con y sin restricciones
==================================================

Se describen las funciones `grafica_2d_con_restricciones`, `grafica_2d_no_restricciones` y `plot_rangos_minimos` que se utilizan para generar gráficas 2D de funciones con y sin restricciones, así como para graficar puntos mínimos para distintas precisiones.

Gráfica 2D de Función con Restricciones
--------------------------------------------

La función `grafica_2d_con_restricciones` genera una gráfica 2D de una función con restricciones para valores de x e y. Se utiliza una grilla de resolución especificada para evaluar la función en cada punto dentro del rango dado de x e y.

Parámetros
~~~~~~~~~~~

- `func` (callable): Función que devuelve el valor de la función en un punto dado.
- `x_range` (tuple, opcional): Rango de valores de x para graficar (default=(-10, 10)).
- `y_range` (tuple, opcional): Rango de valores de y para graficar (default=(-10, 10)).
- `resolution` (int, opcional): Resolución de la grilla para la gráfica (default=400).
- `constraint_value` (float, opcional): Valor de restricción para la función (default=1e6).

Gráfica 2D de Función sin Restricciones
--------------------------------------------

La función `grafica_2d_no_restricciones` genera una gráfica 2D de una función sin restricciones explícitas para valores de x e y. Se utiliza una grilla de resolución especificada para evaluar la función en cada punto dentro de los límites dados de x e y.

Parámetros
~~~~~~~~~~~

- `function` (callable): Función que devuelve el valor de la función en un punto dado.
- `x_limits` (tuple, opcional): Límites de valores de x para graficar (default=(-10, 10)).
- `y_limits` (tuple, opcional): Límites de valores de y para graficar (default=(-10, 10)).
- `num_points` (int, opcional): Número de puntos en cada dimensión para la gráfica (default=100).

Gráfica de Puntos Mínimos para Distintas Precisiones
------------------------------------------------------

La función `plot_rangos_minimos` grafica la función dada y los puntos mínimos encontrados para distintas precisiones utilizando un método univariable de optimización específico.

Parámetros
~~~~~~~~~~~

- `funcion` (callable): Función objetivo que se desea minimizar.
- `a` (float): Límite inferior del rango de búsqueda.
- `b` (float): Límite superior del rango de búsqueda.
- `precisiones` (list): Lista de precisiones para el método de optimización.
- `initial_guess` (float): Valor inicial para el método de optimización.
- `nombre` (str): Nombre del método de optimización a utilizar.
- `n` (int): Número de iteraciones para el método Fibonacci.
- `delta` (float): Parámetro delta para métodos basados en la derivada.

Ejemplo de Uso
----------------

.. code-block:: python
    
    import numpy as np
    import paqueteoptimizacionelizabethrm as op 

    op.utils.grafica_2d_no_restricciones(op.funciones.rastrigin_function)
    op.utils.grafica_2d_no_restricciones(op.funciones.holder_table_function)

    op.utils.grafica_2d_con_restricciones(op.funciones.rosenbrock_with_constraints)
    op.utils.grafica_2d_con_restricciones(op.funciones.townsend_with_constraints)

    op.utils.graficas.plot_rangos_minimos(op.funciones.funcion_3, -2.5, 2.5, [0.5, 0.1, 0.01, 0.0001], 2, "secante", 20, 0.5)
    op.utils.graficas.plot_rangos_minimos(op.funciones.funcion_1, 0.1, 10, [0.5, 0.1, 0.01, 0.0001], 2, "newton", 20, 0.5)
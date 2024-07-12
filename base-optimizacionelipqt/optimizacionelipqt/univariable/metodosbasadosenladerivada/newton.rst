.. _newton_raphson:

Método de Newton-Raphson
============================================================

Utiliza una aproximación lineal de la primera derivada de la función mediante la expansión en serie de Taylor en un punto dado. Esta expresión se iguala a cero para encontrar la siguiente estimación del punto mínimo. Si el punto actual en la iteración t(x), el punto en la siguiente iteración se determina por la ecuación obtenida considerando hasta el término lineal en la expansión de Taylor.

Función `central_difference_f_prime`
-----------------------------

La función `central_difference_f_prime` calcula la derivada primera de una función en un punto dado utilizando el método de diferencias centrales.

Parámetros
~~~~~~~~~~~

- `f` (callable): La función objetivo cuya derivada se quiere calcular.
- `x` (float): El punto en el cual se desea calcular la derivada.
- `delta_x` (float): El pequeño incremento alrededor de `x`.

Retorno
~~~~~~~~~~~

Retorna una aproximación de la derivada primera de la función en `x`.

Función `central_difference_f_double_prime`
---------------------------------

La función `central_difference_f_double_prime` calcula la derivada segunda de una función en un punto dado utilizando el método de diferencias centrales.

Parámetros
~~~~~~~~~~~

- `f` (callable): La función objetivo cuya derivada se quiere calcular.
- `x` (float): El punto en el cual se desea calcular la derivada.
- `delta_x` (float): El pequeño incremento alrededor de `x`.

Retorno
~~~~~~~~~~~

Retorna una aproximación de la derivada segunda de la función en `x`.

Función `delta_x_func`
--------------------

La función `delta_x_func` determina el valor de delta_x en función de x.

Parámetros
~~~~~~~~~~~

- `x` (float): El punto en el cual se desea determinar delta_x.

Retorno
~~~~~~~~~~~

Retorna el valor de delta_x basado en x.

Método de Newton-Raphson
------------------------

La función `newton_raphson_method` implementa el método de Newton-Raphson para encontrar una raíz de una función. Utiliza derivadas de primer y segundo orden calculadas mediante el método de diferencias centrales.

Parámetros
~~~~~~~~~~~

- `funcion` (callable): La función objetivo cuya raíz se desea encontrar.
- `initial_guess` (float): El valor inicial para comenzar la búsqueda de la raíz.
- `delta_x_funcion` (callable): Función que determina el valor de delta_x en función de x.
- `epsilon` (float): La tolerancia para el criterio de convergencia.
- `max_iteraciones` (int, opcional): El número máximo de iteraciones permitidas (por defecto es 10000).

Retorno
~~~~~~~~~~~

La función retorna una aproximación de la raíz de la función.

Ejemplo de uso
~~~~~~~~~~~

.. code-block:: python

    import numpy as np
    import paqueteoptimizacionelizabethrm as op 

    p10 = op.univariable.metodosbasadosenladerivada.newton.newton_raphson_method(op.funciones.funcion_4, np.array([2]), op.univariable.metodosbasadosenladerivada.newton.delta_x_func, 0.0001, 1000)
    print("Algoritmo Newton Función 4", p10)
.. _secante:

Método de la Secante
============================================================

En el método de la secante, se utilizan tanto la magnitud como el signo de las derivadas para generar un nuevo punto. Se asume que la derivada varía linealmente entre dos puntos extremos elegidos. Si las derivadas en los puntos x1 y x2 tienen signos opuestos, existe un punto z entre ellos donde la derivada es cero, que se puede calcular fácilmente. Este método puede eliminar más de la mitad del espacio de búsqueda en una iteración, aunque a veces puede eliminar menos de la mitad.

Función `central_difference_f_prime`
--------------------------

La función `central_difference_f_prime` calcula la derivada primera de una función en un punto dado utilizando el método de diferencias centrales.

Parámetros
~~~~~~~~~~~

- `f` (callable): La función objetivo cuya derivada se quiere calcular.
- `x` (float): El punto en el cual se busca calcular la derivada.
- `delta_x` (float): El pequeño incremento alrededor de `x`.

Retorno
~~~~~~~~~~~

Retorna una aproximación de la derivada primera de la función en `x`.

Función `delta_x_func`
--------------------

La función `delta_x_func` determina el valor de delta_x en función de x.

Parámetros
~~~~~~~~~~~

- `x` (float): El punto en el cual se busca determinar delta_x.

Retorno
~~~~~~~~~~~

Retorna el valor de delta_x basado en x.

Método de la Secante
--------------------

La función `secant_method` implementa un algoritmo de la secante para encontrar un intervalo [x1, x2] donde una función tiene un mínimo local. Se basa en una precisión dada para determinar el tamaño del paso en la búsqueda y utiliza diferencias centrales para calcular la derivada.

Parámetros
~~~~~~~~~~~

- `funcion` (callable): La función objetivo que se busca minimizar.
- `a` (float): Límite inferior del intervalo inicial.
- `b` (float): Límite superior del intervalo inicial.
- `epsilon` (float): La tolerancia para la longitud del intervalo y el valor de la derivada.
- `delta_x` (float): El pequeño incremento utilizado para calcular la derivada.
- `max_iteraciones` (int, opcional): El número máximo de iteraciones permitidas (por defecto es 10000).

Retorno
~~~~~~~~~~~

La función retorna un tuple (x1, x2) que representa el intervalo [x1, x2] que contiene un mínimo local de la función. Si no se encuentra tal intervalo, devuelve None.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python

    import numpy as np
    import paqueteoptimizacionelizabethrm as op 

    p11 = op.univariable.metodosbasadosenladerivada.secante.secant_method(op.funciones.funcion_1, -5, 5, 0.0001, op.univariable.metodosbasadosenladerivada.secante.delta_x_func(1), 1000)
    print("Algoritmo Secante Función 1", p11)
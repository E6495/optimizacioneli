.. _biseccion:

Método de Bisección
============================================================

El método de bisección evita la computación de la segunda derivada y utiliza solo la primera derivada para eliminar partes del espacio de búsqueda. Asume la unimodalidad de la función y requiere dos puntos iniciales que encierren el mínimo. Calcula y compara las derivadas en los puntos límite y en el punto medio, seleccionando dos puntos consecutivos con derivadas de signos opuestos para la siguiente iteración. Este proceso se repite hasta que el mínimo esté adecuadamente delimitado.

Función `central_difference_f_prime`
--------------------------

La función `central_difference_f_prime` calcula la derivada primera de una función en un punto dado utilizando el método de diferencias centrales.

Parámetros
~~~~~~~~~~~

- `f` (callable): La función objetivo cuya derivada se quiere calcular.
- `x` (float): El punto en el cual se desea calcular la derivada.
- `delta_x` (float): El pequeño incremento alrededor de `x`.

Retorno
~~~~~~~~~~~

Retorna una aproximación de la derivada primera de la función en `x`.

Función `delta_x_func`
--------------------

La función `delta_x_func` determina el valor de delta_x en función de x.

Parámetros
~~~~~~~~~~~

- `x` (float): El punto en el cual se desea determinar delta_x.

Retorno
~~~~~~~~~~~

Retorna el valor de delta_x basado en x.

Método de Bisección
-------------------

Parámetros
~~~~~~~~~~~

La función `bisection_method` implementa el método de bisección para encontrar un intervalo [x1, x2] donde una función tiene un mínimo local. Utiliza la derivada primera calculada mediante el método de diferencias centrales para verificar las condiciones iniciales del método.

- `funcion` (callable): La función objetivo que se desea minimizar.
- `a` (float): Límite inferior del intervalo inicial.
- `b` (float): Límite superior del intervalo inicial.
- `epsilon` (float): La tolerancia para la longitud del intervalo y el valor de la derivada.
- `delta_x` (float): El pequeño incremento utilizado para calcular la derivada.
- `max_iteraciones` (int, opcional): El número máximo de iteraciones permitidas (por defecto es 10000).

Retorno
~~~~~~~~~~~

La función retorna un tuple (x1, x2) que representa el intervalo [x1, x2] que contiene un mínimo local de la función.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python

    import numpy as np
    import paqueteoptimizacionelizabethrm as op 

    p9 = op.univariable.metodosbasadosenladerivada.biseccion.bisection_method(op.funciones.funcion_1, np.array([1]), 8, 0.0001, op.univariable.metodosbasadosenladerivada.delta_x_func(1), 1000)
    print("Funcion 1 biseccion", p9)
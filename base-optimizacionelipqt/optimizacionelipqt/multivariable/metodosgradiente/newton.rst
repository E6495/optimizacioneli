.. _newton_section:

Método de Newton (Gradiente)
================

El método de Newton usa las derivadas de segundo orden para crear las direcciones de búsqueda. Lo que permite una mayor velocidad de convergencia. Este método es adecuado y eficiente cuando el punto inicial está cerca del punto óptimo. Sin embargo no se garantiza la reducción de la función objetivo a cada iteración , por lo que, ocasionalmente es necesario reiniciar el punto de inicio.

Implementación del Método de Newton
-----------------------------------

La función `newton` permite varios métodos de búsqueda unidireccional para encontrar un tamaño de paso (`alpha`) adecuado durante cada iteración:

- **Búsqueda Fibonacci**: Utiliza el algoritmo de búsqueda Fibonacci para encontrar `alpha`.
- **Método de Newton-Raphson**: Utiliza el método de Newton-Raphson para encontrar `alpha`.
- **Búsqueda de la Sección Dorada**: Aplica la búsqueda de la sección dorada para determinar `alpha`.
- **Método de Intervalo de Mitad**: Implementa el método de intervalo de mitad para `alpha`.
- **Método de Fase de Limitación**: Utiliza el método de fase de limitación para encontrar `alpha`.
- **Método de Búsqueda Exhaustiva**: Aplica la búsqueda exhaustiva para determinar `alpha`.
- **Método de Bisección**: Implementa el método de bisección para encontrar `alpha`.
- **Método de Secante**: Utiliza el método de la secante para determinar `alpha`.

Función Matriz Hessiana
-----------------------

Calcula la matriz hessiana de la funcion f en un punto x dado.

Parámetros
~~~~~~~~~~~

``f`` (callable): Función cuya matriz hessiana a calcular.
``x`` (array-like): Punto en el cual se evalúa la matriz hessiana.
``deltaX`` (float): Paso para la aproximación numérica de las derivadas parciales.

Retorna
~~~~~~~~~~~

``list of list``: Matriz hessiana de f en x.

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
-------------------

Parámetros
~~~~~~~~~~~

- ``funcion`` (callable): Función objetivo a minimizar.
- ``x0`` (array-like): Punto inicial para la optimización.
- ``epsilon1`` (float): Tolerancia para la norma del gradiente para lograr la convergencia.
- ``epsilon2`` (float): Tolerancia para la diferencia relativa entre iteraciones consecutivas.
- ``M`` (int): Número máximo de iteraciones permitidas.
- ``metodo`` (str): Método para la búsqueda unidireccional ('fibonacci', 'newton', 'dorado', 'interval', 'bounding', 'exhaustiva', 'biseccion', 'secante').

Retorna
~~~~~~~~~~~

- ``np.ndarray``: Punto optimizado que aproxima el mínimo de la función.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python
    
    import numpy as np
    import paqueteoptimizacionelizabethrm as op 

    p7 = op.multivariable.metodosgradiente.newton(op.funciones.himmelblau_function, np.array([1.5, 1.0]), 0.0001, 0.0001, 100, 'dorado')
    print("Algoritmo Newton Gradiente Función Himmelblau", p7)

.. _bounding:

Método de Bounding
=============================================================

El método de la fase de acotación se utiliza para enmarcar el mínimo de una función unimodal. Este método garantiza que el mínimo se encuentre dentro de un intervalo. El algoritmo comienza con una suposición inicial y determina una dirección de búsqueda basada en dos evaluaciones adicionales de la función cercanas a la suposición inicial. Posteriormente, se adopta una estrategia de búsqueda exponencial para alcanzar el óptimo.

Método de Bounding
-----------------------------

La función `bounding_phase_method` utiliza un enfoque iterativo para encontrar un intervalo (a, b) que contiene un mínimo local de una función, basado en una conjetura inicial (`initial_guess`) y un tamaño de paso inicial (`Delta`).

Parámetros
~~~~~~~~~~~

- `funcion` (callable): La función objetivo que se desea minimizar.
- `initial_guess` (float): La conjetura inicial para el punto de inicio.
- `Delta` (float): El tamaño del paso inicial.

Retorno
~~~~~~~~~~~

La función retorna un tuple (a, b) que representa el intervalo que contiene un mínimo local de la función.

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python
    
    import numpy as np
    import paqueteoptimizacionelizabethrm as op 

    p12 = op.univariable.metodoseliminacionderegiones.bounding.bounding_phase_method(op.funciones.funcion_3, 0.6, 0.0001)
    print("Algoritmo Bounding Función 3", p12)

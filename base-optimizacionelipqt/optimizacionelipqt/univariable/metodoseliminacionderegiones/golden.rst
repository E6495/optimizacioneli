.. _golden:

Método de Búsqueda Dorada
===========================================================

El método de búsqueda dorada mapea el espacio de búsqueda (a,b) a un intervalo unitario (0,1). En cada iteración, se eligen dos puntos a una distancia τ de los extremos, asegurando que la región eliminada sea siempre proporcional a la anterior. Esto se logra con τ=0.618, lo que garantiza que uno de los puntos utilizados en cada iteración se considere en la siguiente.

Regla de eliminación
--------------------------

Regla de eliminación para el método de búsqueda dorada.

Parámetros
~~~~~~~~~~~

- `x1` (float): Primer punto de prueba en el intervalo.
- `x2` (float): Segundo punto de prueba en el intervalo.
- `fx1` (float): Valor de la función en x1.
- `fx2` (float): Valor de la función en x2.
- `a` (float): Límite inferior del intervalo actual.
- `b` (float): Límite superior del intervalo actual.

Retorno
~~~~~~~~~~~

tuple: Un nuevo intervalo (a, b) ajustado.

Función conversión de w a x
--------------------------

Convierte un valor w en el intervalo [0, 1] a un valor en el intervalo [a, b].

Parámetros
~~~~~~~~~~~

- `w` (float): Valor en el intervalo [0, 1].
- `a` (float): Límite inferior del intervalo objetivo.
- `b` (float): Límite superior del intervalo objetivo.

Retorno
~~~~~~~~~~~

float: Valor correspondiente en el intervalo [a, b].

Método de Búsqueda Dorada
--------------------------

La función `busquedaDorada` implementa el método de búsqueda dorada, que utiliza la razón áurea para ajustar iterativamente un intervalo [a, b] que contiene un mínimo local de la función objetivo. La función itera hasta que la longitud del intervalo en términos de w (la escala en el intervalo [0, 1]) sea menor que una tolerancia `epsilon`.

Parámetros
~~~~~~~~~~~

- `funcion` (callable): La función objetivo a minimizar.
- `epsilon` (float): La tolerancia para la longitud del intervalo.
- `a` (float): Límite inferior del intervalo inicial. Por defecto es None.
- `b` (float): Límite superior del intervalo inicial. Por defecto es None.

Retorno
~~~~~~~~~~~

La función retorna un float que representa una aproximación del punto que minimiza la función en el intervalo [a, b].

Ejemplo de Uso
~~~~~~~~~~~

.. code-block:: python
    
    import numpy as np
    import paqueteoptimizacionelizabethrm as op 

    p15 = op.univariable.metodoseliminacionderegiones.golden.busquedaDorada(op.funciones.funcion_1, 0.0001, 0.1, 10)
    print("Algoritmo Golden Función 1", p15)
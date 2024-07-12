.. _funciones:

Funciones de Optimización
=========================

Funciones Univariables
----------------------

funcion_clase
^^^^^^^^^^^^^

Calcula la función cuadrática más tres.

:param x: Valor de entrada.
:type x: float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r = op.funciones.funcion_clase(3.5)
        print(r)

funcion_lata
^^^^^^^^^^^^

Calcula la función del volumen de una lata en términos del radio.

:param x: Radio de la lata.
:type x: float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r2 = op.funciones.funcion_lata(3)
        print(r2)


funcion_caja
^^^^^^^^^^^^

Calcula la función para optimizar el volumen de una caja.

:param L: Longitud de la caja.
:type L: float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r3 = op.funciones.funcion_caja(4)
        print(r3)

funcion_1
^^^^^^^^

Calcula una función cuadrática más un término racional.

:param x: Valor de entrada.
:type x: float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r4 = op.funciones.funcion_1(3)
        print(r4)

funcion_2
^^^^^^^^

Calcula una función cúbica con un término lineal y constante.

:param x: Valor de entrada.
:type x: float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r5 = op.funciones.funcion_2(4.5)
        print(r5)

funcion_3
^^^^^^^^

Calcula una función polinómica de cuarto grado con un término cuadrático y constante.

:param x: Valor de entrada.
:type x: float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python
        
        import paqueteoptimizacionelizabethrm as op

        r6 = op.funciones.funcion_3(3)
        print(r6)

funcion_4
^^^^^^^^

Calcula una función polinómica de cuarto grado con términos cúbicos y cuadráticos.

:param x: Valor de entrada.
:type x: float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r7 = op.funciones.funcion_4(3.5)
        print(r7)

Funciones Multivariables
------------------------

rastrigin_function
^^^^^^^^^^^^^^^^^^

Calcula la función de Rastrigin.

:param x: Vector de entrada.
:type x: list of float
:param A: Constante, valor por defecto es 10.
:type A: float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r8 = op.funciones.rastrigin_function([0, 5, 10])
        print(r8)

ackley_function
^^^^^^^^^^^^^^^

Calcula la función de Ackley.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r9 = op.funciones.ackley_function([0, 1])
        print(r9)

sphere_function
^^^^^^^^^^^^^^^

Calcula la función Sphere.

:param x: Vector de entrada.
:type x: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r10 = op.funciones.sphere_function([1, 5, 10])
        print(r10)

rosenbrock_function
^^^^^^^^^^^^^^^^^^^

Calcula la función de Rosenbrock.

:param x: Vector de entrada.
:type x: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r11 = op.funciones.rosenbrock_function([1, 5, 10])
        print(r11)

beale_function
^^^^^^^^^^^^^^

Calcula la función de Beale.

:param x: Vector de entrada de dos dimensiones.
:type x: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r12 = op.funciones.beale_function([1, 2])
        print(r12)

goldstein_price_function
^^^^^^^^^^^^^^^^^^^^^^^^

Calcula la función de Goldstein-Price.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r13 = op.funciones.goldstein_price_function([1, 2])
        print(13)

booth_function
^^^^^^^^^^^^^^

Calcula la función de Booth.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r14 = op.funciones.booth_function([1, 2])
        print(r14)

bukin_function_n6
^^^^^^^^^^^^^^^^^

Calcula la función Bukin N.6.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r15 = op.funciones.bukin_function_n6([1, 2])
        print(r15)

matyas_function
^^^^^^^^^^^^^^^

Calcula la función de Matyas.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r16 = op.funciones.matyas_function([1, 2])
        print(r16)

levy_function
^^^^^^^^^^^^^

Calcula la función de Levy.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r17 = op.funciones.levy_function([1, 2])
        print(r17)

himmelblau_function
^^^^^^^^^^^^^^^^^^^

Calcula la función de Himmelblau.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r18 = op.funciones.himmelblau_function([1, 2])
        print(r18)

three_hump_camel_function
^^^^^^^^^^^^^^^^^^^^^^^^^

Calcula la función de Three-Hump Camel.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r19 =op.funciones.three_hump_camel_function([1, 2])
        print(r19)

easom_function
^^^^^^^^^^^^^^

Calcula la función de Easom.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op
        
        r20 = op.funciones.easom_function([1, 2])
        print(r20)

cross_in_tray_function
^^^^^^^^^^^^^^^^^^^^^^

Calcula la función de Cross-in-Tray.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r21 = op.funciones.cross_in_tray_function([1, 2])
        print(r21)

eggholder_function
^^^^^^^^^^^^^^^^^^

Calcula la función de Eggholder.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float
    
    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r22 = op.funciones.eggholder_function([1, 2])
        print(r22)

holder_table_function
^^^^^^^^^^^^^^^^^^^^^

Calcula la función de Holder Table.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r23 = op.funciones.holder_table_function([1, 2])
        print(r23)

mccormick_function
^^^^^^^^^^^^^^^^^^

Calcula la función de McCormick.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r24 = op.funciones.mccormick_function([1, 2])
        print(r24)

schaffer_function_n2
^^^^^^^^^^^^^^^^^^^^

Calcula la función Schaffer N.2.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r25 = op.funciones.schaffer_function_n2([1, 2])
        print(r25)

schaffer_function_n4
^^^^^^^^^^^^^^^^^^^^

Calcula la función Schaffer N.4.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op 

        r26 = op.funciones.schaffer_function_n4([1, 2])
        print(r26)

styblinski_tang_function
^^^^^^^^^^^^^^^^^^^^^^^^

Calcula la función Styblinski-Tang.

:param X: Vector de entrada de dos dimensiones.
:type X: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r27 = op.funciones.styblinski_tang_function([1, 2])
        print(r27)

shekel_function
^^^^^^^^^^^^^^^

Calcula la función de Shekel.

:param x: Vector de entrada de dos dimensiones.
:type x: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r28 = op.funciones.shekel_function([1, 2])
        print(r28)

rosenbrock_with_constraints
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Calcula la función de Rosenbrock con restricciones.

:param x: Vector de entrada de dos dimensiones.
:type x: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r29 = op.funciones.rosenbrock_with_constraints([1, 2])
        print(r29)

rosenbrock_with_disk_constraint
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Calcula la función de Rosenbrock con una restricción de disco.

:param x: Vector de entrada de dos dimensiones.
:type x: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r30 = op.funciones.rosenbrock_with_disk_constraint([1, 2])
        print(r30)

mishras_bird
^^^^^^^^^^^^

Calcula la función de Mishra's Bird.

:param x: Vector de entrada de dos dimensiones.
:type x: list of float
:returns: Resultado de la función.
:type r: float


    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r31 = op.funciones.mishras_bird([1, 2])
        print(r31)

townsend_with_constraints
^^^^^^^^^^^^^^^^^^^^^^^^^

Calcula la función de Townsend con restricciones.

:param x: Vector de entrada de dos dimensiones.
:type x: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r32 = op.funciones.townsend_with_constraints([1, 2])
        print(r32)

gomez_levy_with_constraints
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Calcula la función de Gomez-Levy con restricciones.

:param x: Vector de entrada de dos dimensiones.
:type x: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r33 = op.funciones.gomez_levy_with_constraints([1, 2])
        print(r33)

simionescu_with_constraints
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Calcula la función de Simionescu con restricciones.

:param x: Vector de entrada de dos dimensiones.
:type x: list of float
:returns: Resultado de la función.
:type r: float

    .. code-block:: python

        import paqueteoptimizacionelizabethrm as op

        r34 = op.funciones.simionescu_with_constraints([1, 2])
        print(r34)
# Paso a paso de como utilizar el Software:

Paso 1: Selección del método

En una “página inicial” el usuario debe seleccionar el método que prefiera utilizar ( el usuario puede elegir entre el método de esquina noroeste y el método de menor costo ), al presionar el botón “seleccionar” del método, es dirigido a su respectiva página listo para que el usuario la use.

Paso 2: Ingreso de datos

El usuario ingresa a la página:
Cantidad de ofertas (orígenes)
Cantidad de demandas (destinos)
Estos valores determinan el tamaño de la matriz del problema.

Paso 3: Generación de la tabla

Al presionar el botón “Generar tabla”, se ejecuta la función:
generarInputs()
Esta función lo que hace es:
Crea una tabla de costos.
Genera los campos de entrada para ofertas y demandas.
Inserta estos elementos en la página.

Paso 4: Ingreso de datos

El usuario completa:
Costos en cada celda
Valores de oferta
Valores de demanda

Paso 5: Validación de totales

Al presionar “Validar Totales”, se ejecuta la función:
calcular()
Esta función lo que hace es:
Suma todas las ofertas
Suma todas las demandas
Compara ambos valores
Al comparar estos valores:
Si son iguales muestra un mensaje de : “datos correctos”
Si son distintos muestra un mensaje de : “Problema no balanceado”.

Paso 6: Equilibrar valores (en caso de que oferta y demanda no sean iguales)

A partir del paso anterior donde se comparan los valores, si oferta y demanda no son iguales, debajo del mensaje explicando que los valores de oferta y demanda no son iguales, aparecerá un botón que solucionaría este problema creando una oferta o demanda “ficticia” que equilibra los valores; en caso de no presionar dicho botón, la página no le permitirá al usuario continuar con el resto del método. 

Paso 7: Resolución del problema

Al presionar “Generar Tabla y Resolver”, se ejecuta la función:
resolverTabla()

Paso 8: Aplicación del método de la esquina noroeste

El algoritmo sigue estos pasos:
Comienza en la celda superior izquierda (posición 0,0)
Compara:
Oferta disponible
Demanda requerida
Asigna el valor mínimo entre ambos
Resta ese valor a oferta o demanda
Se mueve:
Hacia abajo si se agota la oferta
Hacia la derecha si se agota la demanda
Repite el proceso hasta completar la tabla

Paso 9: Visualización de resultados
Se genera una tabla donde:
Cada celda muestra: “asignación | costo”
Las celdas utilizadas se resaltan
Se muestran totales por fila y columna

Paso 10: Calcular la solución inicial
Presionar el botón “Calcular Solución Inicial”.
El sistema calcula:
La suma de: asignación * costo en cada celda
Y muestra el costo total del transporte
Paso 11: Reinicio del sistema
Al presionar “Reiniciar”, se ejecuta la función:
reiniciar()
Lo que hace esto es:
Limpia todos los inputs
Borra la tabla generada
Elimina los resultados
Devuelve la aplicación a su estado inicial

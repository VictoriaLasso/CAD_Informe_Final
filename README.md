# CAD_Informe_Final

Experimento de multiplicación de matrices con OpenMP

Este experimento tiene como objetivo evaluar el rendimiento de la multiplicación de matrices utilizando OpenMP. Se utiliza un procesador de 8 núcleos para realizar el experimento.

### Requisitos ###

Sistema operativo Linux
Compilador C++
OpenMP
Instrucciones

Compile el código con el siguiente comando:
## Multiplicación de matrices filas por filas ##
gcc -fopenmp -O3 Otime.c MM1f.c -o ../BIN/MM1F -lm
Ejecute el código con el siguiente comando:
./MM1F <número de núcleos>
## Multiplicación de matrices de filas por columnas##
gcc -fopenmp -O3 Otime.c MM1c.c -o ../BIN/MM1c -lm

Ejecute el código con el siguiente comando:
./MM1F <número de núcleos>

** Ejecucución de multiples iteraciones **

Para la ejecución de este usamos un iterador en pearl el cual nombramos como lanzador.
```perl

@Ejecutables = ("MM1F"); 
@cores = ("1","2","3","4","5","6","7","8");
@VectorSize= ("100","200","300","400","500");
```
Por ejemplo, para ejecutar el código 30 veces con las anteriores especificaciones lanzamos el siguiente comando:

  ./lanzadorfilas.pl 30
  
Resultados

El código imprimirá el tiempo de ejecución de la multiplicación de matrices para cada número de núcleos en la tabla soluciones.

Análisis

El análisis de los resultados debe incluir una discusión sobre los siguientes puntos:

¿El tiempo de ejecución de la multiplicación de matrices disminuye de forma lineal con el número de núcleos?
¿La multiplicación de filas por filas es el método más eficiente para realizar la operación?

Posibles explicaciones

Si el tiempo de ejecución de la multiplicación de matrices no disminuye de forma lineal con el número de núcleos, es posible que haya factores que estén afectando negativamente al rendimiento, como la carga del sistema o la frecuencia del reloj del procesador.

Si la multiplicación de filas por columnas es más eficiente que la de filas por filas, es posible que el algoritmo de multiplicación de filas por columnas utilizado en el experimento fuera más eficiente que el algoritmo de multiplicación de filas por filas.

Experimentos adicionales

Para determinar la causa del resultado, sería necesario realizar más experimentos utilizando diferentes algoritmos de multiplicación de matrices, condiciones de carga y tamaños de matrices

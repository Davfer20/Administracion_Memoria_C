# Administracion-de-Memoria
## Diego Granados
## Daniel Granados
## David Fernández
Este programa simula la gestión dinámica de memoria en C utilizando las funciones malloc, calloc, realloc y free, a partir de un archivo de entrada que contiene una secuencia de operaciones.

Compilar el programa: "gcc main.c -o main"

Ejecutar el programa: "./main <pruebas.txt>"

Si se desea cambiar el algoritmo de asignación de memoria, se debe cambiar en el archivo de list.c la constante de SORTING_ALGORITHM. 1 es para First Fit, 2 para Best Fit y 3 para Worst Fit.

Si se desea cambiar la cantidad de espacio en la memoria, en el archivo de list.c se debe cambiar la constante de MEMORY_SIZE.

La implementación mantiene dos listas: la lista de procesos activos, que incluye las direcciones de memoria y los tamaños de todos los procesos en uso, y la lista de memoria libre, que muestra las direcciones de memoria disponibles y sus respectivos tamaños.

El programa procesa operaciones a partir de un archivo de entrada, donde cada instrucción debe seguir una sintaxis específica. Para asignar memoria, se utiliza el comando ALLOC en la forma ALLOC <proceso> <tamaño>, donde <proceso> es un carácter identificador (por ejemplo, A) y <tamaño> es un número entero con la cantidad de bytes a asignar.

Para reasignar memoria a un proceso existente, se usa el comando REALLOC con la sintaxis REALLOC <proceso> <nuevo_tamaño>. Para liberar la memoria ocupada por un proceso, se emplea el comando FREE <proceso>. Finalmente, el estado actual de la memoria se imprime utilizando el comando PRINT, que no requiere parámetros adicionales.

ALLOC A 30  
ALLOC B 20  
REALLOC A 40  
FREE B  
PRINT

Al ejecutar el comando PRINT, el programa mostrara detalladamente la lista de procesos asignados, la lista de memoria libre y una representación visual del estado actual de la memoria. Ademas existe una funcion llamada Restore al cual tiene la funcionalidad de restablecer la memoria con el fin de realizar varias pruebas en una sola ejecucion. Esta funcionalidad proporciona una herramienta útil para comprender cómo se gestionan las operaciones de memoria en un sistema operativo, así como para simular y probar escenarios de uso de memoria en aplicaciones reales.

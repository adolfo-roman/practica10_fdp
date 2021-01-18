# Fundamentos de programacion: Practica 10

En esta practica use la antepenultima version de la practica 8
debido a que tiene un problema que no pude ressolver, asi que pense
que seria bueno intentar usar el GDB para ver si puedo entender
que es lo que mi programa esta haciendo mal.

El problema principalmente es que el programa despues de finalizar el segundo
switch, sorpresivamente pasa por alto las instrucciones siguientes y termina
su ejecucion.

1.- Podemos ver que el programa termina su ejecucion.

2.- En la siguiente imagen usamos gcc -g -o enum enum.c para compilar
el programa y que este tenga simbolos de depuracion.

3.- Ejecutamos el programa hasta el punto donde buscamos el error

4.- Al momento de usar la funcion p para que imprima el valor de x
encontramos que esta tiene un valor: 10 '\n'

5.- Mientras investigamos porque x tiene un valor de 10 '\n' encontramos
que e valor en ASCII que tiene '\n' es de 10, es por esta razon que la funcion
scanf al momento de leer el valor de x, lo que encuentra es el valor de
una nueva linea, lo que provoca que se aplique un "enter" y el programa
corra hasta el final consecuentemente.

6.- Procedemos a la correcion del programa.

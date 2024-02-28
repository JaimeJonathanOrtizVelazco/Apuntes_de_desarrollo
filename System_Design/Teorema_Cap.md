# Teorema CAP

De acuerdo con el teorema cap en los sistemas distribuidos. Solamente podemos dar soporte a dos de las siguientes garantías ( medidas de sistema ):

## Consistencia (Consistency)

Cualquier lectura recibe las escritura mas reciente o un error.

## Disponibilidad (Availability)

Cualquier petición recibe una respuesta, sin garantizar que contiene la version mas reciente de información.

## Partition Tolerance

El sistema continua operando sin importar la partición arbitraria debido a fallos de red.

## CP Consistencia / Partición

Esperar una respuesta de la partición puede resultar en un timeout. CP es una buena decision si nuestro sistema requiere de lecturas y escrituras atómicas (ver ACID) .

## AP Disponibilidad/ Partición (Availability/ Partition)

Las respuestas regresan la version mas reciente de la información en cualquier nodo ( es decir el que reciba la petición si es que existen muchos nodos, no podemos saber que información reside en cada nodo). A las escrituras les llevara un tiempo propagarse entre los nodos. Esta es una buena decision si nuestro sistema nos permite la constancia eventual y requerimos que el sistema continue trabajando a pesar de las errores externos.

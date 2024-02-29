# Reverse Proxy (Proxy Inverso)

Un proxy inverso es una tipo de servidor proxy que recupera recursos en nombre de un cliente externo, desde uno o mas servidores internos. Estos recursos se devuelven al cliente como si se originaran en el propio servidor web.

## VS

- Deployar un load balancer es util cuando tiene multiples servidores. Seguido, los load balancer enruta el trafico hacia un conjunto de servidores sirviendo la misma función.

- Soluciones como NGINx o HAProxy pueden soportar el proxy inverso de la capa 7.

## Desventajas

- Introducir un rever proxy resulta en un incremento de la complejidad
- Un solo proxy inverso es una punto unico de falla.

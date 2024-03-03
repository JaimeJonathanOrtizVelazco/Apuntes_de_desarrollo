# Escalado Horizontal / Horizontal Scaling

Los load balancers también pueden ayudar al escalamiento horizontal, mejorando el performance y la disponibilidad. Es mas eficiente en costo y resultados el hacer un escalamiento horizontal que vertical.

## Desventajas

Escalar horizontalmente introduce complejidad e involucra clonar servidores.

- Los servidores deberían ser stateless: significa que no deberían contener información de los usuarios relacionadas con las sesiones.

- Las sesiones pueden ser guardadas in una base de datos centralizada o en un cache persistente (Servidor).

- Los servidores de descarga como bases de datos y cache, necesitan aceptar mas conexiones a como los servidores de carga son escalados

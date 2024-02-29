# Balanceador de carga

Distribuye las peticiones entrantes de un cliente a recursos que dispongan de una aplicación o base de datos. Es como un intermediario entre el servicio y el cliente.

En términos generales el load balancer determina a que servicio se manda la petición del cliente ( servicio que este disponible) y regresa la respuesta del servicio al cliente.

- Previene que las peticiones vayan a servicios no disponibles
- Previene la sobrecarga de los servicios
- Ayuda a eliminar puntos de falla únicos

Los load balancer pueden ser implementados con hardware o con software (HAProxy). Incluye:

- **SSL termination** : Desencripta peticiones entrantes y encripta las respuestas del servidor por lo que servidores backend no tienen que ejecutar estas operaciones costosas.
  - Remueve la necesidad de instalar certificados X.509 en cada servidor.
- **Session persistence (Persistencia de sesiones)** : Provee cookies y eruta una petición especifica del cliente a la misma infancia si la aplicación web no hace el trackeo de las sesiones.

## Desventajas

- Puede crearse un cuello de botella si no hay los recursos suficientes o si no esta configurado de manera correcta.

- Introducir un load balancer puede aumentar la complejidad
- Tener un solo load balancer es tener un punto único de fallo, pero aumentar multiples crea una complejidad mayor.

## [Load Balancer Vs Rever Proxy](Load_Balancer_Reverse_Proxy.md)

## [Load Balancing Algorithms / Algoritmos de Balanceo de Carga](https://)

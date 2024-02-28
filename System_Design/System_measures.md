# El desempeño (Performance) vs la Escalabilidad (Scalability)

Un servicio es escalable si resulta en un incremento del desempeño de manera proporcional a los recursos agregados.

- Si tu sistema tiene problemas de desempeño, tu sistema es lento para un solo usuario.
- Si tu sistema tiene problemas de escalabilidad, es rápido para un usuario pero lento para cargas grandes de trabajo.

# Latencia vs rendimiento (Throughput)

## Latencia (Latency)

La **latencia** se refiere a la cantidad de tiempo que le to al sistema responde a una petición.

## Rendimiento (Throughput)

El **rendimiento (Throughput)** se refiere a la cantidad de peticiones que un sistema puede recibir al mismo tiempo.

Normalmente se espera tener un alto rendimiento con poca latencia.

# Disponibilidad y consistencia

## Disponibilidad (Availability)

Se refiere a la habilidad del sistema de proveer sus servicios a los clientes aun y cuando hay presencia de fallos. Normalmente se mide en terminos del porcentaje del timepo que el sistema esta arriba y corriendo (up and running), tambien conocido como **updatime**.

## Consistencia (Consistency)

Se refiere a la propiedad de que todos los clientes vean la misma informacion al mismo tiempo. Es importante para mantener la integridad de la informacion almacenada en el sistema.

- Normalmente en los sistemas distribuidos, un sistema que prove una alta disponibilidad tiende a sacrificar consistencia, mientras que por el lado contrario, los que proveen una alta consistencia sacrifican disponibilidad.

- Es similar al termino de consistencia de las bases de datos, en donde se espera que los datos esten disponibles una vez una transacion termine.

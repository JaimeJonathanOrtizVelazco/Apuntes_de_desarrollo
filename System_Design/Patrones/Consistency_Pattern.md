# Patron de Consistencia

Se refiere a la manera en que la información es almacenada y manejada en los sistemas distribuidos y como esta información se hace disponible para los usuarios y aplicaciones.

Existen 3 tipos:

## Consistencia Fuerte ( Strong consistency)

A como una actualización es realizada en la información, esta debe ser visible a cualquier operación de lectura subsecuente. La información es reclinada de manera sincronía, asegurando que las copias de la información son actualizadas al mismo tiempo.

## Consistencia Débil (Weak consistency)

Después de que una actualización haya sido hecha en la información, no se garantiza que cualquier petición de lectura subsecuente vaya a reflejar los cambios hechos.

## Consistencia Eventual (Eventual Consistency)

Este tipo es similar a la consistencia débil. Pero a diferencia, en algunos casos si podremos obtener de manera visible los últimos cambios en la información en operaciones subsecuentes de lectura. La información es replicada de manera asíncrona, asegurando que todas las copias de la información son eventualmente actualizadas.

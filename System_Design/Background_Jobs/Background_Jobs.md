# Background Jobs

Se refiere a tareas que se ejecutan en el background de manera independiente del flujo de ejecución principal del sistema. Estas tareas are típicamente iniciadas por el propio sistema en lugar de que sean iniciadas por los usuarios o algún agente externo.

Pueden ser utilizados para varios propósitos:

- Realizar tareas de mantenimientos: Como limpiar información vieja, generar reportes, hacer backups de bases de datos.
- Procesar volúmenes largos de información: tales como importación de información, exportar de información o la transformación de la información.
- Enviar notificaciones
- Realizar computaciones largas, como machine learning o análisis de datos.

## Event-Driven

Usa un trigger para iniciar con una tarea en el background.
Ejemplos:

- La UI u otro trabajo coloca un mensaje en una cola. Este mensaje contiene información acerca de una acción que ha tomado acción (como un histórico). La tarea en el backend toma el mensaje lo procesa. A este tipo de patron se le llamada comunicación basada en mensaje asíncrono.

## Schedule Driven

A como el nombre lo indica se programa el tiempo de ejecución cuando la tarea debe de comenzar.

## Returning Results

Básicamente los trabajos de background no tienen injerencia en las aplicaciones, por lo tanto no es necesario que se espere alguna respuesta de regreso sin que este se haya completado.

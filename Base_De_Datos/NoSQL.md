# NoSQL

Es una colección de información representada con llave-valor, documentos, columnas o grafos. Información desorganizada y la joins se hacen en la aplicación.
La mayoría de bases de datos noSQL tienen problemas con transacciones ACID y fallos eventuales de consistencia.

BASE es comúnmente usada para describir las propiedades de las bases de datos no relaciones. En comparación con CAP, BASE elige la disponibilidad sobre la consistencia.

## (BA) Basically available / Básicamente disponible

El sistema garantiza disponibilidad

## (S) Soft state / Estado blando

El estado del sistema debe cambiar con el tiempo, aun y cuando no hay entrada de datos.

## (E) Eventual Consistency / Consistencia Eventual

El sistema se volverá consistente en un periodo de tiempo, dado que el sistema no recibe información durante un periodo de tiempo.

# Key Value Store

Un almacén de llave-valor permite lecturas y escrituras de O(1) y es normalmente utilizada con memorias o SSD. Estos almacenes de datos pueden mantener llaves lexicográficas en orden, permitiendo la eficiente respuesta de los rangos de llaves.

Los almacenes de llave-valor permite un alto rendimiento y comúnmente son usada para modelos de datos simples o que cambian de manera rápida. Ofrecen un limitado de operaciones, la complejidad es dejada a las aplicaciones.

# Document Store

El almacén de documentos se centra en documentos XML, JSON, binarios u otros, donde un documento almacena toda la información de un objeto. Los almacenes de documentos proven un API o un lenguaje query para buscar información basado en la estructura interna del documento. Muchos almacenes de datos de tipo llave-valor incluyen funcionalidad que funcionan con valores de metadata, fluctuando entre almacenes de documentos y de llave-valor.

Basado en el tipo de implementación, los documentos están organizados por colecciones, tags, metadata o directorios. Ademas lo documentos pueden ser organizados o agrupados juntos.

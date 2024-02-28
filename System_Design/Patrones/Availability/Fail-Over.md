# Fail-Over

Es un patron de disponibilidad que es usado para asegurar que el sistema puede continuar su función en caso de fallas(failure). Esto involucra tener componentes o sistemas de backup para tomar el lugar en caso de fallas.

En un sistema contra fallas, siempre hay un componente primario que es responsable de recibir las peticiones y uns secundario (backup) que se encontrara a la espera (standby).
El componente primario normalmente se encuentra en monitoreo constante y el secundario entra en acción en caso de que el primario presente una falla.

## Active-pasive (Master-slave failover)

En este tipo de patron, peticiones de vida son enviadas al servidor activo y al pasivo en standby. Si la petición es interrumpida, el pasivo toma el lugar del activo para resumir el servicio.

## Active-active

Ambos servidores manejan el trafico y dividen el trafico entre ellos. Si los servidores tienen mascaras publicas, el DNS necesitara saber las IPs publicas de ambos servicios. Si son internas, la aplicación deberá saber sobre ambos servidores.

## Desventajas

- Agregan mayor hardware y complejidad.
- Hay una potencial perdida de información si el sistema falla antes de alguna operación de escritura sea replicada a los sistemas pasivos (backups).

# Replicación (Replication)

La replicación es un patron de disponibilidad que involucra multiples copias de la misma información en diferentes localizaciones. En caso de fallo, la información puede ser consultada de una locación diferente. Existen dos tipos:

## Master-Master

En este tipo de replicación, multiples servidores están configurados como maestro, cada uno de estos acepta operaciones de lectura y escritura. Este tipo de replicación puede llevar a tener conflictos de actualización si multiples servidores intentan actualizar la información al mismo tiempo.

## Master-Slave

Es un tipo de replicación en donde un servidor esta asignado como maestro, aceptando operaciones de escritura, mientras que los esclavos aceptan peticiones de lectura. Si el maestro falla, un esclavo es promovido a maestro.

# Domain Name System (DNS)

Este es el servicio que se encarga de traducir un nombre de dominio a una IP en especifico. Es decir, es como un diccionario de IP, donde se le inserta el nombre del dominio y este te regresara la dirección IP del servidor o servicio que nos interesa consultar.

Los DNS son herarquicos, con algunos servidores autoritarios en un nivel superior. Nuestro router o ISP (Internet Service Provider / Proveedor de Internet) proveerá la información a cerca de que servidor DNS debemos contactar cuando hagamos alguna búsqueda. Los resultados del DNS también pueden ser cacheados (cache / almacenados en cache) de manera local en nuestro navegadores.

- NS record( name server / nombre del servidor) : Especifica el servidor DNS para nuestro dominio o subdominio.
- MX record ( mail exchange ) : Especifica el servidor de correo (mail) para aceptar mensajes.
- A record( address/ dirección) : Apunta el nombre a una dirección IP.
- CNAME (canonical / canónico ) : Apunta el nombre de un dominio a otro o a un A record; (example.com to www.example.com)

## Push CDNs

Reciben el nuevo contenido cuando cambios ocurren en nuestro server. Tomamos la responsabilidad de proveer contenido actualizando directo a una CDN.

## Pull CDNs

Toma el nuevo contenido de nuestros servers cuando el primer usuario solicita el contenido.

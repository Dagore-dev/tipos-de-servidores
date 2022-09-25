# Tipos de servidores

El paradigma cliente-servidor es en estos días la piedra angular del funcionamiento de internet. El ejemplo de aplicación de este paradigma que con más frecuencia y naturalidad se experimenta es el acceso a sitios web. En este ejemplo nuestros equipos pasan a ser clientes de otro servidor o servidores, responsables de servir los ficheros estáticos que la web que visitamos. En este proceso intervienen distintos protocolos (`TCP/IP`, `DNS`, `HTTP`) y equipos. Existen múltiples ejemplos como este en nuestro día a día y en entornos profesionales. En esta presentación se detallarán distintos tipos de servidores y sus características principales.

## Índice

- Servidor `DHCP`
- Servidor `DNS`
- Servidor web
- Servidor de base de datos
- Servidor web `proxy`
- Servidor `FTP`
- Servidor de archivos
- Servidor de aplicación
- Servidor de correo electrónico
- Servidor de impresión
- Servidor de comunicación en tiempo real
- Servidor de servidores virtuales

### Servidor `DHCP`

Un servidor DHCP es un servidor que proporciona y asigna automáticamente direcciones `IP`, puertas de enlace predeterminadas y otros parámetros de red a los dispositivos de los clientes. Se basa en el protocolo estándar conocido como `Dynamic Host Configuration Protocol` o `DHCP` para responder a las consultas de difusión de los clientes [[1]](https://www.infoblox.com/glossary/dhcp-server/).

Este tipo de servidores en entornos no profesionales no son equipos dedicados y los mencionados parámetros de red son determinados por el router o switch. En entornos profesionales un servidor `DHCP` dedicado ofrece a los administradores de sistemas capacidad para automatizar la asignación los parámetros de red definiendo distintas estrategias. Es así que un servidor dedicado permite ajustar correctamente este servicio a la necesidades concretas de forma efectiva.

### Servidor `DNS`

Los servidores `DNS` (`Domain Name System`) son habitualmente descritos como la guía telefónica de internet, esta comparación se ajusta bastante bien a la realidad. Estos servidores son los responsables de la resolución de nombres de dominio, el conjunto de operaciones que permiten convertir una `URL` en una dirección `IP` que identifica al servidor que representa. A día de hoy los servidores `DNS` están bien distribuidos por toda la red y es bastante complicado que fallen [[2](https://www.cloudflare.com/learning/dns/what-is-a-dns-server/)].

Como en el caso de los servidores `DHCP` hay motivos por los que los usuarios (profesionales) pueden querer implementar sus propios servidores `DNS`. Una utilidad de esto puede ser el bloqueo de ciertos dominios, puesto que se pueden establecer reglas para especificar `IP` personalizadas a ciertas direcciones `URL`. Así, por ejemplo, se puede "redireccionar" a un cliente a una web interna donde se le explique que ha intentado acceder a un dominio no permitido en la red donde trabaja.

## Bibliografía

1. [What is a DHCP Server? (Infoblox)](https://www.infoblox.com/glossary/dhcp-server/)
2. [What is a DNS server? (Cloudflare)](https://www.cloudflare.com/learning/dns/what-is-a-dns-server/)

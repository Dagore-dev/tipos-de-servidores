# Tipos de servidores

El paradigma cliente-servidor es en estos días la piedra angular del funcionamiento de internet. El ejemplo de aplicación de este paradigma que con más frecuencia y naturalidad se experimenta es el acceso a sitios web. En este ejemplo nuestros equipos pasan a ser clientes de otro servidor o servidores, responsables de servir los ficheros estáticos que la web que visitamos. En este proceso intervienen distintos protocolos (`TCP/IP`, `DNS`, `HTTP`) y equipos. Existen múltiples ejemplos como este en nuestro día a día y en entornos profesionales. En esta presentación se detallarán distintos tipos de servidores y sus características principales.

## Índice

- Servidor `DHCP`
- Servidor `DNS`
- Servidor web
- Servidor de base de datos
- Servidor web `proxy`
- Servidor `FTP`
- Servidor de aplicación
- Servidor de correo electrónico
- Servidor de impresión
- Servidor virtual

### Servidor `DHCP`

Un servidor DHCP es un servidor que proporciona y asigna automáticamente direcciones `IP`, puertas de enlace predeterminadas y otros parámetros de red a los dispositivos de los clientes. Se basa en el protocolo estándar conocido como `Dynamic Host Configuration Protocol` o `DHCP` para responder a las consultas de difusión de los clientes [[1]](https://www.infoblox.com/glossary/dhcp-server/).

Este tipo de servidores en entornos no profesionales no son equipos dedicados y los mencionados parámetros de red son determinados por el router o switch. En entornos profesionales un servidor `DHCP` dedicado ofrece a los administradores de sistemas capacidad para automatizar la asignación los parámetros de red definiendo distintas estrategias. Es así que un servidor dedicado permite ajustar correctamente este servicio a la necesidades concretas de forma efectiva.

### Servidor `DNS`

Los servidores `DNS` (`Domain Name System`) son habitualmente descritos como la guía telefónica de internet, esta comparación se ajusta bastante bien a la realidad. Estos servidores son los responsables de la resolución de nombres de dominio, el conjunto de operaciones que permiten convertir una `URL` en una dirección `IP` que identifica al servidor que representa. A día de hoy los servidores `DNS` están bien distribuidos por toda la red y es bastante complicado que fallen [[2](https://www.cloudflare.com/learning/dns/what-is-a-dns-server/)].

Como en el caso de los servidores `DHCP` hay motivos por los que los usuarios (profesionales) pueden querer implementar sus propios servidores `DNS`. Una utilidad de esto puede ser el bloqueo de ciertos dominios, puesto que se pueden establecer reglas para especificar `IP` personalizadas a ciertas direcciones `URL`. Así, por ejemplo, se puede "redireccionar" a un cliente a una web interna donde se le explique que ha intentado acceder a un dominio no permitido en la red donde trabaja.

### Servidor Web

Un servidor web en su mínima expresión es un servidor `HTTP` (`Hypertext Transfer Protocol`) que utiliza este protocolo para manejar peticiones de recursos a través de la red (sea esta internet o algún tipo de red local). Los sitios web que podemos visitar con nuestro navegador se alojan en este tipo de servidores donde se guardan o generan los ficheros estáticos que recibe el cliente (`HTML`, `CSS`, `JS`, imágenes, ...) [[3]](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server).

Los sitios web siguen principalmente dos estrategias para alojarse en estos servidores: pueden ser sitios web estáticos o dinámicos. Un sitio web estático simplemente almacena en el servidor web los ficheros estáticos que pretende servir al cliente, por contra, los sitios web dinámicos actualizan la totalidad o una parte de los estáticos antes de enviarlos en respuesta a una petición `HTTP`. Las web dinámicas presentan una mayor complejidad y por eso habitualmente necesitan servidores de aplicación y de base de datos (serán discutidos más adelante) [[3]](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server).

### Servidor de base de datos

Los servidores de base de datos alojan y ejecutan un `DBMS` (`DataBase Management System`) junto con la información que almacena la base de datos. Estos servidores exponen una interfaz a los clientes para que interaccionen con la base de datos. La interfaz puede definir diversas medidas o estrategias de seguridad para que el acceso y modificación de los datos lo realicen solo clientes debidamente autenticados [[4]](https://phoenixnap.com/kb/what-is-a-database-server).

Existen múltiples servidores de base de datos, tanto relacionales (`SQL`) como no relacionales (`noSQL`) cada uno con sus características únicas, decidir adecuadamente la que se ajusta a las necesidades de nuestra aplicación u organización es una tarea de elevada complejidad que no debe tomarse a la ligera.

### Servidor web `proxy`

Un servidor `proxy` actúa como intermediario entre un recurso y un cliente que quiere acceder a este. Así se simplifica la complejidad de la solicitud y otorga beneficios adicionales, como balanceo de carga, privacidad o seguridad. Por lo tanto, un servidor proxy funciona en nombre del cliente cuando solicita un servicio, enmascarando potencialmente el verdadero origen de la solicitud al servidor de recursos [[5]](https://en.wikipedia.org/wiki/Proxy_server).

### Servidor `FTP`

Los servidores `FTP` utilizan el `File Transfer Protocol` para que los clientes puedan descargar y subir ficheros a un almacenamiento compartido. Es posiblemente una de las formas más sencillas y económicas a disposición de las organizaciones que necesitan compartir información entre sus miembros dentro de una red local o internet. Para acceder a los ficheros guardados en este tipo de servidores se puede emplear un navegador web, aunque existen también clientes especializados como `Filezilla` que presentan ciertas ventajas, especialmente cuando se trabaja con ficheros de gran tamaño [[6]](https://www.techopedia.com/definition/26108/ftp-server).

### Servidor de aplicación

Un servidor de aplicación contiene lógica de negocio y trabaja conjuntamente con servidores web y servidores de base de datos. Las aplicaciones web dinámicas emplean este tipo de servidores porque proveen `Server Side Rendering` (`SSR`), es decir, ante una petición concreta pueden generar los ficheros estáticos necesarios procesando la información que viene con la petición y/o recuperando información de un servidor de base de datos [[7]](https://www.nginx.com/resources/glossary/application-server-vs-web-server/).

Estos servidores no necesariamente tienen que estar acoplados a un servicio web concreto, pueden exponerse para funcionar como `APIs` públicas (`Application Program Interface`) que reciban y respondan peticiones.

### Servidor de correo electrónico

Los servidores de correo emplean el `Simple mail transfer protocol` (`SMTP`) para enviar y recibir correos electrónicos a través de la red que los destinatarios obtienen mediante el `Post Office Protocol` (`POP`). Estos servidores emplean un sistema de dominios para identificar a dónde deben ser enviados los mensajes, dichos dominios son definidos tras la `@` en el nombre del correo electrónico. En consecuencia, para tener un dominio propio y personalizado se necesita un servidor de correo electrónico [[8]](https://www.samlogic.net/articles/mail-server.htm).

### Servidor de impresión

Un servidor de impresión conecta impresoras a clientes a través de una red. Acepta trabajos de impresión de las clientes y los envía a las impresoras apropiadas, poniendo los trabajos en cola localmente para adaptarse al hecho de que el trabajo puede llegar más rápido de lo que la impresora realmente puede manejar. Las funciones auxiliares incluyen la capacidad de inspeccionar la cola de trabajos a procesar y de reordenar o eliminar trabajos de impresión en espera. Los servidores de impresión se pueden utilizar para hacer cumplir las políticas de administración, como cuotas de impresión en color, autenticación de usuario/departamento o documentos impresos con marcas de agua [[9]](https://en.wikipedia.org/wiki/Print_server).

### Servidor virtual

Un servidor virtual reproduce las funciones de un servidor físico dedicado. Existe de forma transparente para los usuarios como un espacio con particiones dentro de un servidor físico. La virtualización de servidores facilita la reasignación de recursos y se adapta a las cargas de trabajo dinámicas [[10]](https://cloud.google.com/learn/what-is-a-virtual-server). 

## Bibliografía

1. [What is a DHCP Server? (Infoblox, 25/09/2022)](https://www.infoblox.com/glossary/dhcp-server/)
2. [What is a DNS server? (Cloudflare, 25/09/2022)](https://www.cloudflare.com/learning/dns/what-is-a-dns-server/)
3. [What is a web server? (MDN, 25/09/2022)](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server)
4. [What Is a Database Server & What Is It Used For? (phoenixNAP, 25/09/2022)](https://phoenixnap.com/kb/what-is-a-database-server)
5. [Proxy server (Wikipedia, 25/09/2022)](https://en.wikipedia.org/wiki/Proxy_server)
6. [FTP Server (Techopedia, 25/09/2022)](https://www.techopedia.com/definition/26108/ftp-server)
7. [What Is an Application Server vs. a Web Server? (NGINX, 25/09/2022)](https://www.nginx.com/resources/glossary/application-server-vs-web-server/)
8. [What is a Mail Server and How Does it Work? (Samlogic, 25/09/2022)](https://www.samlogic.net/articles/mail-server.htm)
9. [Print Server (Wikipedia, 25/09/2022)](https://en.wikipedia.org/wiki/Print_server)
10. [¿Qué es un servidor virtual? (Google Cloud, 25/09/2022)](https://cloud.google.com/learn/what-is-a-virtual-server)

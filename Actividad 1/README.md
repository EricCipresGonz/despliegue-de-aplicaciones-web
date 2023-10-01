
3. Analiza los headers de las peticiones cuando inicias sesión en el Moodle y comprende
cómo se obtiene el token. Para ello, necesitamos saber de dónde salen TODOS los
datos sensibles que se envían.

![tempsnip](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/d1501db1-b009-4db1-82fc-8c741048208b)

· Lo que hay que hacer es una vez dentro de la zona de iniciar sesion del moodle es hacer click derecho en la pagina y darle a inspecionar, una vez dentro le damos a Network le damos a index.php y vamos al apartado de Payload y tendremos el resultado


4. ¿A qué puerto se reciben normalmente las peticiones del protocolo HTTP? ¿A qué
capa del modelo TCP/IP se encuentra el protocolo HTTP? ¿Y los protocolos TCP,
UDP, e IP?

· Normalmente se utiliza en el puerto 80 para las comunicaciones no seguras y el puerto 443 para comunicaciones seguras, el protocolo TCP/IP se encuentra en la capa de aplicaciones en la capa 4. Los protocolos TCP se encuentra en la capa 4, el protocolo UPD en la capa 4, i el protocolo de la IP esta en la capa 3

5. ¿Cuál es el significado de la siguiente respuesta de un servidor?
HTTP/1.1 302 Found
Location: http://www.example.com/test/index2.php

·El 302 Found con el Location significa para redirigir al cliente a una nueva ubicación

6. Utilizando el filtro de captura para la interfaz de red de Wireshark, analiza la petición
al host: www.google.com. Mostrando la cabecera IP, la dirección IP de tu ordenador y
la del servidor. Comprueba que, poniendo esa IP en el navegador, accedas a Google

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/a69ee329-5cce-4dc6-a78d-31538ef90d4b)

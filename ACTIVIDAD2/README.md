1. Instale en una máquina virtual un sistema operativo con base Linux (se recomienda Debian o Ubuntu) e instale apache2. .
   
 ![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/7cc2a489-2a8c-4c44-8a28-c8286bce53c6)
 

3. Explique con sus palabras que es una petición GET, POST, PUT y DELETE, remarcando sus diferencias. .  

El GET se utiliza para solicitar datos del servidor  

El POST se utiliza para enviar datos al servidor para que lo procese 

El PUT se utiliza para enviar datos al servidor para crear o actualizar un recurso 

El DELETE se utiliza para eliminar un recurso especifico en el servidor 


 

3. Cambie del puerto 80 al puerto 4444 el servidor apache2. Muestra desde el navegador su funcionamiento adjuntando una captura de pantalla. .  


Bueno primero en /etc/apache2/ports.conf cambiamos el Listen 80 por el 4444 








![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/55354da2-70ab-4a6a-9981-4ef284b169f3)







Una vez hecho eso reiniciamos el apache 












![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/e91b4fdb-cd5b-4ed7-b355-aa4526836668)












I por ultimo vamos al navegador i ponemos localhost:4444 en el buscador y te tiene que devolver lo siguiente: 













![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/73e5dec9-1830-4c5a-b2c0-4fa555570e6c)


4. Instale un certificado SSL y configure su Apache para servir contenido a través de HTTPS en el puerto 4444. Muestre desde el navegador cómo se muestra el sitio web como "seguro" (aunque sea un certificado autofirmado). .  

Primero generamos un certificado con el siguiente comando: 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/4e959e98-f587-4070-bb4e-9b82d1e20559)








Despues en el archivo sudo nano/etc/apache2/sites-available/tu_sitio.conf lo rellenamos con lo siguiente: 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/4da81108-c971-4b93-8648-90c4507dc9df)











Despues hay que hablilitar el modulo SSL con los siguientes comandos: 


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/21a893fe-f2b0-4568-9e5e-218732814e5b)




Reiniciamos el apache y  podemos ver en el navegador que funciona correctamente 




![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/05ca144f-83c2-439d-b787-92dcc1ea9455)





5. ¿Dónde se encuentran los ficheros de configuración de Apache2?  

• Ubicación principal. 

Se encuentra en el archivo /etc/apache2/apache2.conf 

 • Explora el archivo apache2.conf. Identifica las secciones principales y describe su propósito.  
 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/79e0bfa5-afe8-4453-b2ec-63088ac67dd8)




• sites-available y sites-enabled: Explica la diferencia entre estos dos directorios y cómo funcionan juntos.  

sites-available contiene los archivos de configuracion de los sitios virutales , y el enable contiene los enlaced simbolicos a los arcihvos de la configuracion. 

• mods-available y mods-enabled: Explica la diferencia entre estos dos directorios. .  

Mods-available significa que se pueden utilizar y enables son aquellos mods que no se estan ejecutando o que no tienes. 

6. ¿Dónde se encuentran los ficheros de ejecución de Apache2? 

 • Ubicación principal  

/etc/init.d/apache2 

• Control del servicio: Utiliza el binario de ejecución para iniciar, detener, recargar y reiniciar el servidor Apache2 explicando la diferencia entre cada uno de los comandos utilizados.  

El Start: Este comando sirve para iniciar el servidor 

El Stop: Este comando sirve para detener el servidor 

El Reload: Este comando sirve para recargar el servidor 

El Restart: Este comando sirve para reiniciar el servidor 


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/a8d29b52-3efd-4edc-8a90-f66252700ecc)



• Comprobación de sintaxis: Usa el binario de Apache para verificar la sintaxis de tu configuración. Esto es útil para asegurarse de que no haya errores antes de reiniciar el servidor. .  


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/bcc44957-a803-4ffd-bd57-5276bd7f5d78)



7. ¿Dónde se encuentran los ficheros de monitorización de Apache2?  

• Ubicación principal  

/etc/apache2/ 

• error.log y access.log: Explica la diferencia entre estos dos archivos. Abre y revisa las entradas recientes en cada uno de ellos. 

El error.log registra los errores y advierte al servidor Apache 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/86fedd71-a5e1-45c4-86ab-e791794c4a5c)


Y el access.log registra los detalles que estan de las solicitudes de acceso al servidor Apache.Cada vez que se pide un acceso se registra aqui. 


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/4450b37b-6a4c-47bb-ab22-6ef2a18bbafb)



• Rotación de logs: Investiga cómo funciona la rotación de logs en Apache2. ¿Por qué es importante? ¿Cómo se configura?  

Es importante porque ahorra espacio de almacenamiento, mejora el rendimiento y por último mantenimiento de registros. 

La configuración es de la siguiente manera: 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/2703fe16-2022-49b0-887e-5fea519641f7)



 Monitorización en tiempo real: Utiliza herramientas como tail -f para monitorear en tiempo real los accesos a tu servidor web y posibles errores.  

 ![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/65eb7399-60da-428e-8ee7-20b4957bf130)

• Análisis de logs: Instala y usa herramientas como goaccess para analizar y obtener estadísticas visuales a partir de tus logs de Apache2. . 



![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/b585bc80-dea9-4e98-917f-615cb82797eb)


8. ¿Qué es un Firewall? ¿Para qué sirve? ¿Por qué es necesario? Instale y configure un Firewall en la máquina virtual para que solo permita tráfico HTTP y HTTPS. Bloquee todo el resto de los puertos y demuestre su funcionamiento. .  

El Firewall es una barrera que tiene la función de proteger una red de cualquier amenaza. 

Y también tiene la función de filtrar el tráfico de archivos y información que entra y sala en la red. Es necesario para tener una red segura en todo el rato. 

Instalación: 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/d309df2f-577b-4c72-a4fa-330ea55a5121)


Miramos que esta inactivo : 


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/7a3a754d-21b9-4563-8c56-e3cc27f82041)



![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/f7214762-3afe-4d9a-b29f-09fc72c9c721)


Y ahora lo activamos 



![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/36d3de4f-d15b-4c92-9336-821bacf3fb8f)




![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/48181ca3-946c-4c0e-9375-701b3165536a)




![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/d2ce1ec2-2141-4467-83ba-74d94b889a61)




9. Explica con tus palabras las diferentes partes de una URL. .  

Parte1: Protocolo= Indica que clase de protocolo se utiliza como el HTTPS o HTTP el primero es mas seguro que el segundo 

Parte2: Dominio= Es el nombre del sitio web que accedemos 

Parte3: Ruta= Ubicación situada exacta del recurso dentro de la web 

Parte4: Fragmento= Referencia de una sección especial dentro del recurso 

Parte5: Parámetros= Son valores adicionales que se pueden pasar a la pagina web  

10. Explica el funcionamiento del protocolo HTTP con tus palabras. . 

- Primeramente, la solicitud del navegador cuando introduces una dirección web en tu navegador, el navegador crea una solicitud HTTP que incluye la URL y otros datos como cookies. 

- Segundo, él envió de la solicitud al servidor, es decir el navegador envía una solicitud al servidor que aloja la página web mediante el HTTP. 

- Tercero, el procesamiento en el servidor es cuando el servidor recibe la solicitud y la procesa 

- Cuarto, la generación de la respuesta que consiste en que el servidor crea una respuesta HTTP que incluye la información solicitada. 

- Cinco, el envió de la respuesta al navegador, el servidor envía esta respuesta de vuelta al navegador a través del HTTP 

- Y por último el procesamiento en el navegador, que consiste en que el navegador recibe la respuesta y procesa los datos. 

 11. ¿Qué es un archivo .htaccess? Proporcione un ejemplo de cómo se puede utilizar para reescribir URL o restringir el acceso a ciertas partes de su sitio web. 

Es un archivo de configuración utilizado en servidores web Apache para controlar y personalizar la configuración del servidor a nivel de directorios y archivos. Permite definir reglas y directivas para modificar el comportamiento del servidor, incluyendo la reescritura de URLs y la restricción de acceso a ciertas partes del sitio web. 

 

 

Con el siguiente comando podemos reescribir la URL 

 

RewriteEngine On  

 RewriteRule ^articulo/([a-zA-Z0-9_-]+)$ articulo.php?id=$1 [NC,L] 

 

Y con el siguiente podemos restringir el acceso 

 

<Files "archivo-restringido.html"> Require valid-user </Files> 

 


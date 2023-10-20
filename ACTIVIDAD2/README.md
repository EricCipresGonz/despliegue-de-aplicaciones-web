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

P3: Módulos de Apache 

 

1. Añade en tu servidor el módulo mod_info y explique para que se utiliza este plugin. . 

Primeramente, hay que hacer el siguiente comando para ver si está en funcionamiento

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/5940a37f-1b75-4d68-aa1b-df3f6f4df3e1)


Después en el archivo nano /etc/apache2/sites-available/ssl.conf hacemos lo siguiente: 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/86ac9ec8-50ad-4db0-8219-94dfc9502a6f)

Y por ultimo reiniciamos el servidor 

Y en el navegador ponemos nuestra ip / server-info: 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/9b59802f-b563-4024-8f97-4b3c94f9ec91)

Bueno en la página web podemos ver que la información sobre la configuración y el estado del servidor apache. El mod_info se utiliza para obtener información sobre el servidor Apache y de su configuración  

2. Oculta la versión del sistema y sistema de apache. .  

Para ocultar la versión del sistema hay que añadirle las dos líneas del final al archivo /etc/apache2/apache2.conf 


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/7e8faed1-a482-4202-a03a-8c7e0a844265)

3. Crea una carpeta en la raíz del path del servidor con el nombre public y otra con el nombre private. Permite que la carpeta public se visualice y el resto de las carpetas que se creen, incluyendo private, no se muestren. A continuación, puede observar cómo se debe de mostrar la carpeta public: 

 

Primero creamos los siguientes directorios:  

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/41edb6de-a9bf-48cf-926a-cc6a65bc150a)

Después les damos permisos 


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/8d9c384a-1e36-479b-9077-26379b1a5017)


Por último vamos a el buscador y ponemos nuestra ip /public 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/0b16749a-d3f2-4e33-b865-89cde7f48878)


4.Prueba de acceder poniendo www. delante de tu URL actual. ¿Funciona? En caso negativo, haz que funcione mediante el módulo mod_rewrite. Investigue como utilizar el archivo .htacess para implementarlo. .  

Hacemos el siguiente touch: 


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/130967ff-ee57-498e-ad30-979cb37845e1)


Y despues un nano donde vamos a poner lo siguiente: 


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/84f3b151-4250-4f90-ac33-1a7614ce0c4c)

Y ya funcionaria. 

 

 

5. Muestra los directorios de Apache con un tema diferente. Puedes utilizar https://github.com/ramlmn/Apache-Directory-Listing u otra alternativa que te llame la atención. 

 

Ahora vamos a utilizar los siguientes comandos: 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/84f6f115-2f02-4aab-85fc-e6c3c151d9fd)



En el archivo de si.conf he puesto lo siguiente: 

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/9d39b5a1-d0d3-459c-bf89-529c3f280b77)

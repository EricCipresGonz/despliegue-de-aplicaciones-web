
1. Crea dos sitios web que compartirán IP y puerto, pero tendrán nombres DNS distintos
para acceder a ellos. El nombre del primer dominio será daw.gimbernat.eug.es y el
segundo tunombreyapellidos.gimbernat.eug.es, donde “tunombreyapellidos” contiene
la inicial de tu nombre, el primer apellido, y la inicial de tu segundo apellido. De esta
manera, si tu nombre es: Francisco Mesas Cervilla, el domino quedaría:
fmesasc.gimbernat.eug.es.
• En el primer caso, daw.gimbernat.eug.es tendrá su directorio base en
/var/www/daw/ conteniendo una página llamada index.html que ponga el
nombre de la clase como título con un archivo css para aplicarle estilos al título.
• En el segundo caso, fmesasc.gimbernat.eug.es tendrá su directorio base en
/var/www/fmesasc/ (el equivalente para vuestros nombres), conteniendo una
página llamada index.html que contenga vuestro currículum aplicándole un
estilo css para que se visualice correctamente.
Para ello, tendrás que crear un archivo de configuración (copiado de 000-default.conf)
para cada uno de los dominios. Recuerda que con a2ensite puedes crear los enlaces
simbólicos necesarios para añadir esta configuración a la ejecución de apache.


Primero vamos a crear los siguientes directorios


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/2cf12ed1-b430-4826-a9e2-2a589008d35d)



Ahora dentro de el directorio de daw creamos un archivo html y uno css:

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/0ba16f6a-b9c4-4660-8f50-9b1dff34ddb2)



![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/80bc5fb0-5750-4d36-a2e4-ffda2ad29691)




Y volvemos ha hacer lo mismo pero en el directorio de ecipresg pero el html sera el curriculum;


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/7ae70021-aebc-4a4d-826f-3191968e34c0)



![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/5986b109-3688-4fed-a3a6-2a55a394aa32)

Y ahora vamos a /etc/hosts y ponemos lo siguiente:


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/f59b106b-526d-404d-9164-d8852b45327f)

Ahora hacemos lo siguiente:
![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/dbc95607-98e4-45e4-9255-def5076862af)



![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/c7d4765c-705f-4dbf-8e6c-29e7e808dd19)


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/afdb935f-89e3-4cff-93fc-f666b8ecbe26)



Una vez hecho eso ejecutamos los siguientes comandos


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/b5dc73fc-3a01-4bcb-84df-96640edc6f4e)


Y al buscar en la barra de navegacion podremos ver el resultado final:

![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/a81d88e2-6710-444d-bba5-c03d86d7b346)


![image](https://github.com/EricCipresGonz/despliegue-de-aplicaciones-web/assets/144775307/7498afd3-f390-4656-9474-8e04126b645a)

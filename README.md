El archivo DockerFile es el mismo para las tres apps (red, green y yellow) se debe de copiar en cada carpeta.

Para evitar tener que levantar dos veces el proyecto (una para el proxy y otra para el balanceador), el balanceador utiiza el puerto 80. 
De esta forma con un solo docker-compose up -d se levantarían la applicación nginx-proxy, con cada app en un puerto diferente 
(red-app en localhost:3000, yellow-app en localhost:4000 y green-app en localhost:5000)
Y nginx-balancer la levanntamos en el puerto :80, de esta forma podemos acceder al balanceador a través de localhost y con cada actualización muestra una app diferente. 

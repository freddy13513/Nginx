### Versión de Nginx instalado.

![image](/img/10.jpg)

### Ficheros de configuración.

www/var/htlm

![image](/img/11.jpg)

### Modifica la página web que lanza por defecto y personalízala.

![image](/img/12.jpg)

![image](/img/13.jpg)

### Balanceo de carga desde https
En esta práctica voy a usar tres máquinas virtuales. Dos harán de servidores y una de balanceador de carga.

Maquina 1
Lo primero le añado una tarjeta de red interna con la ip 192.168.100.1
![image](/img/14.jpg)

Instalo Nginx y configuro la pafina por defecto
![image](/img/15.jpg)

modificamos el fichero /etc/hosts y le añadimos la pagina que he creado antes 
![image](/img/16.jpg)

comprobamos desde el navegador 
![image](/img/17.jpg)

Maquina 2 volvemos a repetir el proceso anterior  le añado una tarjeta de red interna pero en este caso con la ip 192.168.100.2 
![image](/img/18.jpg)

Instalo Nginx y configuro la pafina por defecto
![image](/img/19.jpg)

modificamos el fichero /etc/hosts y le añadimos la pagina que he creado antes 
![image](/img/20.jpg)

comprobamos desde el navegador 
![image](/img/21.jpg)


Máquina 3 (balanceador de carga)

Para esta máquina, al igual que las otras dos, le añado la tarjeta de red interna con la IP 192.168.100.3

![image](/img/22.jpg)

Instalo nginx. Elimino el archivo de configuración por defecto y creo el nuevo archivo de configuración del balanceador de carga.

![image](/img/23.jpg)

Edito el fichero y le añado los dos servidores
![image](/img/24.jpg)

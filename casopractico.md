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

Modificamos el fichero /etc/hosts y le añadimos la pagina que he creado antes 

![image](/img/16.jpg)

Comprobamos desde el navegador 

![image](/img/17.jpg)

Maquina 2 volvemos a repetir el proceso anterior  le añado una tarjeta de red interna pero en este caso con la ip 192.168.100.2 

![image](/img/18.jpg)

Instalo Nginx y configuro la pagina por defecto

![image](/img/19.jpg)

Modificamos el fichero /etc/hosts y le añadimos la pagina que he creado antes 

![image](/img/20.jpg)

Comprobamos desde el navegador 

![image](/img/21.jpg)


Máquina 3 (balanceador de carga)

Para esta máquina, al igual que las otras dos, le añado la tarjeta de red interna con la IP 192.168.100.3

![image](/img/22.jpg)

Instalo nginx. Elimino el archivo de configuración por defecto y creo el nuevo archivo de configuración del balanceador de carga.

![image](/img/23.jpg)

![image](/img/24.jpg)

Edito el fichero y le añado los dos servidores

![image](/img/25.jpg)

Compruebo la sintaxis con el comando

![image](/img/26.jpg)

Una vez que la sintaxis está correcta, modifico el fichero /etc/hosts añadiendo la IP del balanceador de carga y la página
www.freddy206.com

![image](/img/27.jpg)

Reincio el servicio de nginx y compruebo desde el navegador que está balanceando la carga.

![image](/img/28.jpg)
![image](/img/29.jpg)

### Habilitar https

Para habilitar https, primero necesito instalar el paquete openssl en el baalanceador de carga
apt install openssl

![image](/img/30.jpg)

creo un nuevo directorio para los certificados

mkdir /etc/nginx/certificate

![image](/img/31.jpg)

Entro en la carpeta y creo la clave privada y el certificado mediante el comando openssl

openssl req -new -newkey rsa:4096 -x509 -sha256 -days 365 -nodes -out nginx-certificate.crt -keyout nginx.key

![image](/img/32.jpg)

Modifico el fichero de configuración del balanceador de carga

![image](/img/33.jpg)

Compruebo la sintaxis

nginx -t

![image](/img/34.jpg)

Compruebo desde el navegaador

![image](/img/35.jpg)












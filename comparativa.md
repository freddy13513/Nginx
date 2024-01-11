## Compartiva entre Apache y Nginx

Por un lado tenemos Apache que es el servidor web más popular actualmente gracias a su gran compatibilidad de potencia, su simplicidad arquitectónica y un soporte multiplataforma muy útil. Por otro lado tenemos Nginx que al igual que Apache también es un servidor HTTP de código abierto y gratuito. Tambíen puede ser usado como proxy TCP/UDP, como proxy de correo y como proxy inverso. Nginx usa recursos mínimos para servir a un gran número de usuarios, lo que es un problema para Apache pero que nginx ha sabido resolver.

### Diferencias

En cuanto al sistema operativo, ambos funcionan bien con UNIX/LINUX pero si se quiere usar Windows, Apache es mejor opción.
La administración y mantenimiento de Apache viene dada por una comunidad de desarrollos y la de Nginx por la propia empresa que lo creó.
Apahe tiene un solo hilo asociado a una sola conexión y Nginx es capaz de manejar miles de conexiones que se gestionan simultáneamente reduciendo la memoria, aumentando la velocidad y mejorando el rendimiento.
Nginx tiene una arquitectura basada en eventos para poder administrar varias solicitudes de clientes permitiendole tener un rendimiento mayor incluso si se trata de un tráfico pesado. Apache no es capaz de esto ya que tiene una arquitectura de subprocesos múltiples que hacen dificil esta escalabilidad.
Apache procesa contenido dinámico de forma nativa dentro del propio servidor, Nginx no tiene esta capacidad si no que depende de procesos que se ejecutan externamente.

![image](/img/avsn.jpg)

El programa funciona de la siguiente manera:

1. Se ha de ejecutar en consola el archivo KKMultiServer.java

2. A la hora de ejecutarlo, escribiremos el puerto en el que va a 
atender la llamada que el cliente realizará tal que así:
java KKMultiServer 4444 .

3. A continuación se podrán ejecutar múltiples clientes mediante el 
archivo KnockKnockClient.java mediante el siguiente código:
java KnockKnockClient.java (direción ip en la que está el servidor) 
(puerto de escucha del servidor). Ej: java KnockKnockClient 192.168.1.2 
4444 .

¿Qué hace el programa?

Cada vez que el servidor recibe una nueva llamada crea un nuevo objeto 
enchufe o shocket desde el cual activará un nuevo hilo de conexión que 
habrá de seguir el protocolo de comunicación almacenado en el archivo 
KnockKnockProtocol. A partir de aquí la comunicación simplemente se 
establece y fluye en ambos sentidos.

Por su parte, el cliente recibe la dirección con la que habrá de 
comunicarse y el puerto de destino de la misma. Una vez establece la 
conexión está preparado para almacenar en memoria volátil o buffer la 
entrada del usuario y enviarla al servidor que responderá en función de 
su protocolo.



# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado o utilizó otros comandos que no se mencionan al realizar la práctica también se debe documentar.

##Mi Aprendizaje
Conceptos que aprendí:
- Volumen: Sirve para poder almacenar/guardar información de uno o varios contenedores. Es decir, que si tu tienes datos en un contenedor y lo eliminas, estos datos se peirden con él, pero si creas un volumen pues esto no pasa, conservas los datos así elimines el contenedor. *Se crea al junto el contenedor*.
  
 Si le das a dos contenedores el mismo volúmen (usb para podner ejemplo), cualquiera puede manipular los datos, así el 1 sea quien necesita editar y leer, miestras que el otro   solo leer, para quitar este riesgo se usa el read only. Es decir que estos permiten hacer un estilo de copias de sguridad o de trabajo colaborativo.
 
 Existen algunos tipos de almacenamiento:
 1. Bind mount: En pocas palabras es darle un directorio de tu sistema (host) para que se trabaje como volúmen.
    ```
    docker run -d --name <nombre contenedor> -v <ruta carpeta host>:<ruta carpeta contenedor> <imagen> 
    ```
    ```
    docker run -d --name <nombre contenedor> --mount type=bind,source=<ruta carpeta host>,target=<ruta carpeta contenedor> <imagen>
    ```
 3. Volumen: Docker tiene un espacio ya definido en el host y es lo que va a usar.
 4. TMPFS: Memoria temporal, no persistente


 Comandos (ambos para volumen):
 1. --volume o -v
 2. --mount

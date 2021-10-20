
version: '2'    #versión de docker compose que se va a utilizar.

services:   #declaración de los servicios que se van a poner en funcionamiento.
  dns:
    image: internetsystemsconsortium/bind9:9.16   #declaración de la imagen que se va a utilizar para el servicio.
    ports:
    - 53:53   #mapeo entre el puerto real y el puerto del contenedor que se va a utilizar.
    volumes:    #indicación de las rutas de de cada uno de los volumenes 
      - volume1:/etc/bind
      - volume2:/var/cache/bind
      - volume3:/var/lib/bind
      - volume4:/var/log
volumes:    #indicación de los volumenes que se deben crear.
    volume1:
    volume2:
    volume3:
    volume4:  

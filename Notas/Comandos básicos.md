## Comandos básicos

##### Crea un contenedor

```bash
$ docker container create (nombre del contenedor)
```

##### Ejecuta un contenedor

```bash
$ docker container start (nombre del contenedor)
```

##### Listar contenedores

```bash
//Lista los contendores en ejecución
$ docker container ls 

//Lista los contendores locales 
$ docker container ls -a
```

##### Eliminar un contenedor

```bash
//Listar contenedores 
$ docker container ls -a

CONTAINER ID   IMAGE               COMMAND             CREATED          STATUS                     PORTS     NAMES
74451c37436c   fernando93d/hello   "python ./app.py"   11 minutes ago   Exited (0) 3 minutes ago             dazzling_nash


$ docker container remove (container id o container name)
```

##### Descargar una imagen

```bash
$ docker image pull (nombre de la imagen)

$ docker image pull ubuntu:version

$ docker image pull ngnix:version


/*El nombre de la version es opcional, en caso de no especificarlo, 
descarga la imagen mas reciente */
```

##### Ejecutar una terminal de una imagen en la misma consola

```bash
$ docker container run -it (nombre de la imagen)

$ docker container run -it ubuntu


//Para este caso usamos la flag i para especificar que queremos 
mantener el servicio 

//Y la -t para abrir la terminal de la imagen 
```

La desventaja de ejecutar así el contenedor, será que al finalizar el proceso se perderá la ejecución y al listar los contendores activos no lo podremos ver.

![WhatsApp Image 2022-10-22 at 20.04.02.jpeg](/home/genaro-javier/Descargas/WhatsApp%20Image%202022-10-22%20at%2020.04.02.jpeg)

![Screenshot_20221022_201238.png](/home/genaro-javier/Descargas/Screenshot_20221022_201238.png)

Esto lo podemos arreglar si agregar el flag -d que especifica que se ejecute en segundo plano. 

![](/home/genaro-javier/.config/marktext/images/2022-10-22-20-19-51-image.png)

De esta forma ya podemos ejecutar el contenedor de ubuntu en segundo plano. 

![](/home/genaro-javier/.config/marktext/images/2022-10-22-20-20-55-image.png)

Otro ejemplo ahora ejecutando NGINX 

#### Notas adicionales

Un contenedor se apaga cuando no tiene ningún proceso corriendo. 

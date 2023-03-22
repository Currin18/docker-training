#

Levantar un contenedor
```
docker run postgres
docker run postgres:11.0
```

Descargar una imagen del Repositorio de Docker (Registry)
```
docker pull ubuntu
```

Manejo de imágenes
```
docker images
docker image history postgres
```

Mostrar contenedores
```
docker ps
docker ps -a
```

Controlar ejecución de contenedores
```
docker stop <ID|NAME>
docker start <ID|NAME>
```

Mostrar logs de un contenedor
```
docker logs <ID|NAME>
docker logs -f <ID|NAME>
```
! Importante: No escribir en un fichero, siempre al standar output

Ejecutar comandos sobre un contenedor
```
docker exec <ID|NAME> COMMAND
docker exec -it <ID|NAME> COMMAND
```


Crear una nueva red
```
docker network create todo-app
```

Correr MySQL dentro de la red
```
docker run -d \
--network todo-app --network-alias mysql \
-v $(pwd)/.db:/var/lib/mysql \
-e MYSQL_ROOT_PASSWORD=secret \
-e MYSQL_DATABASE=todos \
mysql:5.7

// On Mac M1 add: --platform linux/x86_64
```

Entrar al contenedor y lanzar comandos SQL
```
docker exec -it <ID|NAME> mysql -p
> show databases;
```

Correr contenedor con herramientas de red
```
docker run -it --network todo-app nicolaka/netshoot
> dig mysql
```

Correr versión v2 de app dentro de la red y conectando a la BD
```
docker run -p 3000:3000 \
--network todo-app \
-e MYSQL_HOST=mysql \
-e MYSQL_USER=root \
-e MYSQL_PASSWORD=secret \
-e MYSQL_DB=todos \
app:v2
```
CMD vs ENTRYPOINT
* CMD para comandos estáticos
* ENTRYPOINT para pasar parámetros (ej: cambiar el fichero de inicio)

Construir imágenes
```
docker build .
docker build -t app .
```

Correr imágenes y levantar contenedores
```
docker run -d app
docker run -dp 3000:3000 app
```
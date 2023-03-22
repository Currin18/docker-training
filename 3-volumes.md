Vincular un volumen al contenedor
```
docker run -v $(pwd)/.data:/etc/todos -dp 3000:3000 app

// edit file /src/static/js/app.js:109
docker run -v $(pwd)/.data:/etc/todos -v $(pwd)/src:/app/src -dp 3000:3000 app
```

Volver a construir la imagen con un nuevo tag
```
docker build -t app:v2 .
```
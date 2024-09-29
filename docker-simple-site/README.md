Sí, puedes exponer tu sitio localmente utilizando Docker. Aquí tienes un ejemplo de cómo hacerlo:

1. Crea un archivo `Dockerfile` en el mismo directorio que tu `index.html` con el siguiente contenido:
    ```Dockerfile
    FROM nginx:alpine
    COPY . /usr/share/nginx/html
    ```

2. Construye la imagen de Docker:
    ```sh
    docker build -t mi-sitio-web .
    ```

3. Ejecuta un contenedor con la imagen creada:
    ```sh
    docker run -d -p 8080:80 mi-sitio-web
    ```

Esto expondrá tu sitio web en `http://localhost:8080`. Cualquier cambio que hagas en los archivos locales no se reflejará automáticamente en el contenedor, por lo que necesitarás reconstruir la imagen y reiniciar el contenedor para ver los cambios.
# Usa la imagen base de Nginx
FROM nginx:alpine

# Copia los archivos del sitio web al directorio de Nginx
COPY . /usr/share/nginx/html

# Expone el puerto 80
EXPOSE 80

# Comando para ejecutar Nginx en primer plano
CMD ["nginx", "-g", "daemon off;"]
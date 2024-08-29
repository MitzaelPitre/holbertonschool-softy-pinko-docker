# Usa la imagen base de Nginx más reciente
FROM nginx:latest

# Copia los archivos del frontend al directorio adecuado en el contenedor
COPY softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copia el archivo de configuración de Nginx al contenedor
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expon el puerto en el que Nginx escuchará
EXPOSE 9000

# El contenedor usará el comando por defecto para iniciar Nginx
CMD ["nginx", "-g", "daemon off;"]

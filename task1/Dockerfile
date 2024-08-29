# Usa la última imagen de Ubuntu
FROM ubuntu:latest

# Actualiza y actualiza los paquetes
RUN apt-get update && apt-get upgrade -y

# Instala Python3 y pip3
RUN apt-get install -y python3 python3-pip

# Elimina el archivo EXTERNALLY-MANAGED para evitar problemas de instalación
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Instala Flask
RUN pip3 install flask

# Define el directorio de trabajo
WORKDIR /app

# Copia el archivo Python a la imagen
COPY ./api.py /app/api.py

# Exponer el puerto que Flask utilizará
EXPOSE 5252

# Comando por defecto para ejecutar la aplicación Flask
CMD ["python3", "api.py"]



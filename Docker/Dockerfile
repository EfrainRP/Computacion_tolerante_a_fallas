#Dockerfile, nos permitira construir y correr una IMAGEN a nuestra necesidades
# Utlizara la imagen base de NodeJs version 18
FROM node:18   

# RUN ejecutara el comando, creando la carpeta para guardar el codigo fuente EN EL CONTENEDOR que se esta creando
#se usa commandos de Linux 
RUN mkdir -p /home/app

# Nos permite acceder a los archivos del sistema anfitrion(Windows) para pasarlo al CONTENDOR("Linux")
COPY . /home/app

#Nos permite pasar los paquetes que necesitamos para esta aplicacion Web a nuestro lugar de trabajo del contenedor
COPY package*.json /home/app  

#Expone el puerto para que otros CONTENEDORES y/o sistema anfitrion puedan comunicarse/accedan a ESTE CONTENEDOR
EXPOSE 3000

#Comando a ejecutar para que la aplicacion empiece su ejecucion, "comando" + "argumentos"
RUN npm install
CMD ["node", "/home/app/index.js"]

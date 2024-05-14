# Usa la imagen base de Node.js
FROM node:latest

# Establece el directorio de trabajo en /app
WORKDIR /app

# Copia el archivo package.json al directorio de trabajo
COPY package.json .

# Instala las dependencias utilizando Yarn
RUN yarn install

# Copia los archivos de la aplicación al directorio de trabajo
COPY . .

# Construye la aplicación
RUN yarn build

# Exponer el puerto 8080 para que la aplicación Vue.js sea accesible desde fuera del contenedor
EXPOSE 8080

# Comando para ejecutar la aplicación Vue.js
CMD ["yarn", "serve"]

# NodeJs Base image
FROM node:12
# Create working directory
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
# Copiamo i due file di packaging
COPY package*.json ./

# Installiamo tutti i pacchetti
RUN npm ci 
# Bundle app source
# Copiamo il resto del codice sorgente
COPY . .
# Esponiamo la porta dove l'applicazione è in esecuzione
EXPOSE 8080
# Comando npm run dev che verrà eseguito dentro il container
CMD [ "npm", "run", "dev" ]

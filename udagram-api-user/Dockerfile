FROM node:13
# Créer le répertoire de l'application
WORKDIR /usr/src/app
# Installer les dépendances de l'application
# Un joker est utilisé pour s'assurer que le paquet.json ET le paquet-lock.json sont copiés lorsqu'ils sont disponibles (npm@5+)
COPY package*.json ./
#Lancez npm ci
RUN npm ci 
RUN npm install typescript@latest

# Regroupement des sources de l'application
COPY . .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]
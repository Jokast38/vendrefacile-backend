# Utilise une image Node.js officielle légère
FROM node:20-alpine

# Crée le dossier de travail dans le conteneur
WORKDIR /app

# Copie les fichiers package.json et package-lock.json s'ils existent
COPY package*.json ./

# Installe les dépendances
RUN npm install

# Copie le reste du code source
COPY . .

# Expose le port utilisé par le service
EXPOSE 8005

# Commande de démarrage
CMD ["npm", "start"]

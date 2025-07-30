# frontend/Dockerfile

# Image de base
FROM node:20

# Dossier de travail
WORKDIR /app

# Copier les dépendances
COPY package*.json ./

# Installer les dépendances
RUN npm install

# Copier tout le projet
COPY . .

# Exposer le port
EXPOSE 3000

# Démarrer l'app
CMD ["npm", "start"]

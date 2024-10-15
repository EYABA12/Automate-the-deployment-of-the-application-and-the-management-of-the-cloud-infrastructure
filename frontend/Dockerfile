################################ staging ####################################
# Étape de construction (staging)
FROM node:14 AS build
# Définir le répertoire de travail à /app
WORKDIR /app
# Copier les fichiers package.json et package-lock.json dans le répertoire de travail
COPY package*.json ./
RUN npm cache clean --force
# Installer les dépendances
RUN apt-get update && apt-get install -y git \
    && npm install --legacy-peer-deps
RUN npm install socket.io-client
# Copier le reste de l'application dans le répertoire de travail
COPY . .
# Construire l'application pour la production
RUN npm run build
################################# production ####################################
# Étape finale (production)
FROM nginx:latest
# Copier le build de l'application à partir de l'étape de build précédente
COPY --from=build app/build  /usr/share/nginx/html
# Copier le fichier de configuration nginx
COPY nginx.conf /etc/nginx/nginx.conf
# Exposer le port 80
EXPOSE 80
# Commande pour démarrer nginx en mode daemon
CMD ["nginx", "-g", "daemon off;"]

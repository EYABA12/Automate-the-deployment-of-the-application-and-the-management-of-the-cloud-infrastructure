# Étape de construction (staging)
FROM node:14 AS build
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install --save-dev @types/eslint @types/estree
RUN npm install -f
COPY . .
EXPOSE 4002
CMD ["npm", "start"]

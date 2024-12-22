FROM node:18

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm install

# Instalar nodemon globalmente
RUN npm install -g nodemon

COPY . .

EXPOSE 80
CMD ["nodemon", "index.js"]

FROM node:18

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm install

RUN npm install -g nodemon

COPY . .

EXPOSE 9001

CMD ["nodemon", "index.js"]

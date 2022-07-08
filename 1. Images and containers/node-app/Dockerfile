FROM node:16-alpine3.15

WORKDIR /node-app

# package.json copied first to avoid the unecessary execution of npm install
COPY package.json .

RUN npm install

COPY . /node-app

EXPOSE 3000

CMD ["node", "server.js"]
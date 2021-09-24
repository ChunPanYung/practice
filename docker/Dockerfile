<<<<<<< HEAD
FROM node:alpine
COPY . /app
WORKDIR /app
CMD node app.js
=======
FROM node

ENV  MONGO_DB_USERNAME=admin \
     MONGO_DB_PWD=password

RUN  mkdir -p /home/app

COPY . /home/app

CMD ["node", "server.js"]
>>>>>>> docker

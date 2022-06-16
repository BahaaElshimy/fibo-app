from node:14.14.0-alpine

workdir /app

copy package.json /app

RUN  npm install

copy . .

cmd ["npm" , "run" ,  "start"]
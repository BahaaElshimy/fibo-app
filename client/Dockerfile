from node:16-alpine

workdir /app

copy package.json /app

RUN  npm install

RUN mkdir node_modules/.cache && chmod -R 777 node_modules/.cache


copy . .

cmd ["npm" , "run" ,  "start"]


from nginx
expose 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
copy --from=builder /app/build /usr/share/nginx/html
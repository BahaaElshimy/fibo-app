from node:16-alpine as builder

workdir /app

copy package.json /app

RUN  npm install

copy . .

cmd ["npm" , "run" ,  "build"]


from nginx
expose 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
copy --from=builder /app/build /usr/share/nginx/html
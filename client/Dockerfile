
# Node container 
FROM node:alpine as builder

#every command should run inside of ...
WORKDIR /app
# copy pkg json into folder
COPY ./package*.json ./
# create node modules inside of docker image
RUN npm install
#copy everything from build context (first .) and put it into this directory (second .)
COPY . . 
RUN npm run build

FROM nginx

EXPOSE 3000

COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf

COPY --from=builder /app/build /usr/share/nginx/html

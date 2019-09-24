# Size on container only 112 MB

FROM node:alpine as build-stage

WORKDIR /usr/src/app
RUN chown node /usr/src/app
COPY package*.json ./
COPY . .
RUN npm install
RUN npm run build

FROM nginx
COPY --from=build-stage /usr/src/app/dist /usr/share/nginx/html

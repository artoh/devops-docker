FROM node:alpine

WORKDIR /usr/src/app
RUN chown node /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 5000
ENV API_URL=http://localhost:7000
USER node
CMD ["npm","start"]

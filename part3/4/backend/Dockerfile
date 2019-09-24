FROM node:alpine

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

RUN	chown node -R /usr/src/app
USER node

EXPOSE 8000

ENV FRONT_URL="http://localhost:5000"

CMD ["npm","start"]

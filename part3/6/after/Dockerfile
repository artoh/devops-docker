FROM alpine

WORKDIR /usr/src/app
RUN apk add --no-cache nodejs npm tesseract-ocr tesseract-ocr-data-fin poppler-utils imagemagick ghostscript && \
  adduser -D ocr

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 4004

USER ocr

CMD ["node","index.js"]

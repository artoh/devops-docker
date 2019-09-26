FROM ubuntu

WORKDIR /usr/src/app
RUN apt-get update && apt-get install -y nodejs npm tesseract-ocr tesseract-ocr-fin poppler-utils imagemagick ghostscript


COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 4004

CMD ["node","index.js"]

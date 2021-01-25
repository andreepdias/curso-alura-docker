FROM node:latest
LABEL André Eduardo Pacheco Dias
WORKDIR /var/www
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD node .
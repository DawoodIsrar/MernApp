FROM node:18.9.1

WORKDIR /app

COPY package.json .

RUN npm config set registry https://registry.npmjs.org/


RUN npm install

COPY . .

EXPOSE 5050

CMD ["npm", "start"]


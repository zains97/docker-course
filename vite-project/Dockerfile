FROM node:alpine

RUN addgroup zains-group && adduser -S -G zains-group zain

USER zain

WORKDIR /app

COPY package*.json .

USER root

RUN chown -R zain:zains-group .

USER zain

RUN npm install

COPY . .

EXPOSE 5173

CMD npm run dev



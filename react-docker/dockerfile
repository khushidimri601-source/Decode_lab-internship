FROM node:20-alpine

RUN addgroup -S app && adduser -S app -G app

WORKDIR /app

COPY package*.json ./

RUN chown -R app:app /app

USER app

RUN npm install

COPY . .

EXPOSE 5173

CMD ["npm", "run", "dev"]


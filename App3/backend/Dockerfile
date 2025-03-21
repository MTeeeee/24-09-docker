FROM node:22-alpine3.20

WORKDIR /backend
COPY package.json package-lock.json ./
RUN npm install --omit=dev

COPY . .

EXPOSE 3050

CMD ["node", "server.js"]
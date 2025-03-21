FROM node:22-alpine3.20

# Define build-time arguments
ARG DB_USER
ARG DB_PASSWORD
ARG DB_NAME
ARG DB_HOST
ARG DB_PORT

# Convert ARGs to ENV variables inside the container
ENV DB_USER=$DB_USER
ENV DB_PASSWORD=$DB_PASSWORD
ENV DB_NAME=$DB_NAME
ENV DB_HOST=$DB_HOST
ENV DB_PORT=$DB_PORT

WORKDIR /backend
COPY package.json package-lock.json ./
RUN npm install --omit=dev

COPY . .

EXPOSE 3050

CMD ["node", "server.js"]
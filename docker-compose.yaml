version: "3.7"
services:
  app:
    container_name: knote-app
    image: learnitguide/knotejs:1.0
    environment:
           MONGO_URL: mongodb://mongo_db_host:27017/dev
    ports:
     - "80:3000"
    depends_on:
     - mongo
    links:
      - mongo:mongo_db_host
  mongo:
    container_name: knote-mongo
    image: mongo

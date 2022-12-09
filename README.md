# Dockerfile-and-Docker-CLI-syntax
(Hobby) Here is an explanation how Dockerfile and Docker CLI syntax can be understood and used

```
FROM node 

WORKDIR /app 

COPY . /app 

RUN npm install

EXPOSE 80 

CMD ["node", "server.js"]
```

node is the image from Dockerhub. It includes Linux. WORKDIR sets "/app" as default working directory. COPY copies the content into the app folder. RUN 
builds the container. EXPOSE 80 exposes port 80 for listening. CMD starts the container. 


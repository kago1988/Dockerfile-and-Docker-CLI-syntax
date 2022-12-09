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

`FROM` node says: node is the image from Dockerhub. It includes Linux. `WORKDIR` sets "/app" as default working directory. `COPY` copies the content into 
the app folder. `RUN` builds the container. `EXPOSE 80` exposes `port 80` for listening. `CMD` starts the container.  
<br />
`Docker build .` builds a custom image.  
<br />
`Docker run <id>` starts the container.  
<br />
`Docker run -p 3000:80 <id>` let's you access the web-app on `localhost:3000`. `3000:80` means that inside the vm port `80` is listening.  
<br />
If you make changes, for example on the `server.js`, you need to rebuild your Docker image with `Docker build .`.  
<br />

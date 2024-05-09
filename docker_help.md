# Docker Help

This file is based off [this link](https://docs.docker.com/get-started/02_our_app/).

Create Dockerfile
```bash
touch Dockerfile
```

Here is a template dockerfile
```bash
# syntax=docker/dockerfile:1

FROM node:18-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000
```

Build docker image
```bash
sudo docker build -t getting-started .
```

Run container
```bash
sudo docker run -dp 127.0.0.1:3000:3000 getting-started
```

View active containers
```bash
sudo docker ps
```

Stop and remove container
```bash
sudo docker stop <container-id>
sudo docker rm <container-id>
```

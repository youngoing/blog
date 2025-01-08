# Dockerfile
FROM registry.cn-beijing.aliyuncs.com/k8w/node:16 AS build
WORKDIR /app
COPY package*.json ./
RUN npm install
RUN npm config set registry https://registry.npmmirror.com
RUN npm run build

WORKDIR /app
COPY . .
EXPOSE 3000
CMD ["npm", "start"]

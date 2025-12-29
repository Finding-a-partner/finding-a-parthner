FROM node:18-alpine

WORKDIR /app

# Устанавливаем китайское зеркало для npm
RUN npm config set registry https://registry.npmmirror.com/

COPY package.json ./
RUN npm install --network-timeout 600000

COPY . .

EXPOSE 3000
CMD ["npm", "start"]
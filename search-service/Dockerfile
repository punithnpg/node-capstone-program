FROM node:10

# Create app directory
WORKDIR /src/search-service

COPY package.json ./

# Install app dependencies
RUN npm install

RUN npm install pm2 -g

# Bundle app source
COPY . .

EXPOSE 3000

CMD ["pm2", "start", "/src/search-service/pm2.config.js"]
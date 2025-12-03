FROM node:20
WORKDIR /opt/server
EXPOSE 8080
COPY package.json .
COPY *.js .
RUN npm install
ENV MONGO="true" \
    REDIS_URL="redis://redis:6379/redis" \
    MONGO_URL="mongodb://mongodb:27017/users"
    # MONGO_URL="mongodb://mongodb:172.17.0.2/catalogue" \    
CMD ["node", "server.js"]



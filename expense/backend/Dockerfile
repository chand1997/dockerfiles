FROM node:20-alpine
RUN addgroup -S expense && adduser -S expense -G expense
# this is how we create user, group and assign user to group in alpine.
RUN mkdir /opt/backend
RUN chown -R expense:expense /opt/backend
WORKDIR /opt/backend
COPY package.json .
COPY *.js ./
RUN npm install
ENV DB_HOST="mysql"

# ENV DB_HOST="localhost"
#if we are using --network host during run, we have to use DB_HOST="localhost"

# "mysql" is container name of mysql.

USER expense
CMD ["node","index.js"]

# In default network containers cannot communicate(if we try-->err: mysql not found).
# so we have to create our own network.

# docker network create <network-name>

# docker network connect  <network-name> <container-name> 
#       --> connecting already created containers to network

# docker run -d --name=<container-name> --network=<network-name> <image-name>:<tag> 
#       --> creating container directly in the network

# docker network inspect <network-name>
#    --> to check which containers attached to network.


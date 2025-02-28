FROM node:20-alpine
RUN addgroup -S expense && adduser -S expense -G expense
# this is how we create user, group and assign user to group.
RUN mkdir /opt/backend
RUN chown -R expense:expense /opt/backend
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"

# ENV DB_HOST="localhost"
#if we are using --network host during run, we have to use DB_HOST="localhost"

# "mysql" is container name of mysql.

USER expense
CMD ["node","index.js"]
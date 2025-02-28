FROM node:20-alpine
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"

# ENV DB_HOST="localhost"
#if we are using --network host during run, we have to use DB_HOST="localhost"

# "mysql" is container name of mysql.
CMD ["node","index.js"]
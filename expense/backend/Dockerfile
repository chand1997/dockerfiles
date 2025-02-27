FROM node:20
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"
# "mysql" is container name of mysql.
CMD ["node","index.js"]
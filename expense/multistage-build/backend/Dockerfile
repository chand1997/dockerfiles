FROM node:20-alpine as build
WORKDIR /opt/backend
COPY package.json .
COPY *.js ./
RUN npm install


FROM node:20-alpine 
RUN addgroup -S expense && adduser -S expense -G expense
RUN mkdir /opt/backend
RUN chown -R expense:expense /opt/backend
ENV DB_HOST="mysql"
COPY --from=build /opt/backend /opt/backend
USER expense
CMD ["node","index.js"]







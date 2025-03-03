FROM node:20-alpine AS build
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



# We are basically passing run time dependencies only to second stage and build/developement time dependencies 
# will remain in first stage which will be removed eventually after this line-->"COPY --from=build" 
# thats how we are reducing image size.






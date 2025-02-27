FROM nginx:latest
RUN rm -rf /usr/share/nginx/html/index.html
COPY index.html /usr/share/nginx/html/index.html

# since we are using base image as nginx , we dont have to use CMD to start nginx again
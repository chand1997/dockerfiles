FROM nginx:latest
RUN rm -rf /usr/share/nginx/html/index.html
ONBUILD COPY index.html /usr/share/nginx/html/index.html

#above ONBUILD code only works, when this image is used as the base image of other image.

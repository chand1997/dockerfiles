FROM nginx:latest
RUN rm -rf /usr/share/nginx/html/index.html
ADD --chmod=400 https://raw.githubusercontent.com/chand1997/dockerfiles/refs/heads/main/CMD/Dockerfile /usr/share/nginx/html/index.html

# or you can add this for chmod

# RUN chmod +r /usr/share/nginx/html/index.html
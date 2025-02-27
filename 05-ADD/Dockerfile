FROM nginx:latest
RUN rm -rf /usr/share/nginx/html/index.html
ADD --chmod=555 https://raw.githubusercontent.com/chand1997/dockerfiles/refs/heads/main/CMD/Dockerfile /usr/share/nginx/html/index.html

# or you can add below line for chmod by removing --chmod=555 from above line.

# RUN chmod +r /usr/share/nginx/html/index.html 


# another usecase of ADD  
ADD sample-1.tar /tmp/
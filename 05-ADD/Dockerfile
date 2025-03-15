FROM nginx:latest
RUN rm -rf /usr/share/nginx/html/index.html
ADD https://www.w3.org/TR/png/iso_8859-1.txt /usr/share/nginx/html/index.html

# or you can add below line for chmod by removing --chmod=555 from above line.

RUN chmod +r /usr/share/nginx/html/index.html 


# another usecase of ADD  
ADD sample-1.tar /tmp/


# COPY is used to copy files from the local system to the container.

# ADD can also copy files but additionally supports remote URLs(but here we have to add permissions like --chmod=555 or chmod +r otherwise 403 forbidden error) and automatic archive extraction(i.e .tar files).
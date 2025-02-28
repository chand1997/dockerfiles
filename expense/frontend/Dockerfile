# FROM nginx:alpine
# RUN rm -rf /usr/share/nginx/html/index.html
# RUN rm -rf /etc/nginx/nginx.conf
# COPY nginx.conf /etc/nginx/nginx.conf 
# COPY code /usr/share/nginx/html/


FROM nginx:alpine


RUN rm /etc/nginx/nginx.conf /etc/nginx/conf.d/default.conf


RUN apt-get update && apt-get upgrade -y \
    && apt install nano curl -y \ 
    && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /var/cache/nginx/client_temp && \
        mkdir -p /var/cache/nginx/proxy_temp && \
        mkdir -p /var/cache/nginx/fastcgi_temp && \
        mkdir -p /var/cache/nginx/uwsgi_temp && \
        mkdir -p /var/cache/nginx/scgi_temp && \
        chown -R nginx:nginx /var/cache/nginx && \
        chown -R nginx:nginx /etc/nginx/ && \
        chmod -R 755 /etc/nginx/ && \
        chown -R nginx:nginx /var/log/nginx

RUN mkdir -p /etc/nginx/ssl/ && \
    chown -R nginx:nginx /etc/nginx/ssl/ && \
    chmod -R 755 /etc/nginx/ssl/

RUN touch /var/run/nginx.pid && \
        chown -R nginx:nginx /var/run/nginx.pid /run/nginx.pid

RUN rm -rf /usr/share/nginx/html/index.html
RUN rm -rf /etc/nginx/nginx.conf
COPY nginx.conf /etc/nginx/nginx.conf 
COPY code /usr/share/nginx/html/

USER nginx

CMD ["nginx", "-g", "daemon off;"]
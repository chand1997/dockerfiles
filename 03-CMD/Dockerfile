FROM almalinux:9
RUN dnf install nginx -y
CMD ["nginx","-g","daemon off;"]


# RUN is used to execute commands at build time(creating the image).
# CMD is used to define the default command executed at container runtime.
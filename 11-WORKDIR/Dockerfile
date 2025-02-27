FROM almalinux:9
RUN mkdir /tmp/work_dir
RUN cd /tmp/work_dir
# here cd doesnt work and pwd gives /, and hello.txt will be created in root directory.

RUN pwd

RUN echo "Hello from Chandan" > hello.txt
CMD ["sleep","100"]

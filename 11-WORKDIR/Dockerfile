FROM almalinux:9
RUN mkdir /tmp/work_dir

# RUN cd /tmp/work_dir
# here cd doesnt work and pwd gives /, and hello.txt will be created in root directory.

WORKDIR /tmp/work_dir
# By using WORKDIR pwd changes to /tmp/work_dir and hello.txt will be created in that directory.

RUN pwd

RUN echo "Hello from Chandan" > hello.txt
CMD ["sleep","100"]

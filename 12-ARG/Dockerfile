ARG version
RUN echo "${version}" > /tmp/devops.txt
FROM almalinux:${version:-9}
# in the above line if we dont provide version during image build using --build-args, it will take 9 as version.
ARG user="Chandan"
RUN echo "${user}" > /tmp/user.txt
ENV user=$user
CMD ["sleep","100"]


#ARG can be accessed only during the image build, if we want to access the ARG inside container,
# we can save them using echo or creating env as shown above
#(we should not do any of these by the way) 







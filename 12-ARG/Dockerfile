ARG version
FROM almalinux:${version:-9}
# in the above line if we dont provide version during image build using --build-arg version=8, it will take 9 as version.
RUN echo "$version" > /tmp/devops.txt
# we dont get version in devops.txt because ARG declared before FROM cannot be accessed after FROM.
ARG user="Chandan"
ENV user=$user
RUN echo "${user}" > /tmp/user.txt

CMD ["sleep","100"]


#ARG can be accessed only during the image build, if we want to access the ARG inside container,
# we can save them using echo or creating env as shown above
#(we should not do any of these by the way) 







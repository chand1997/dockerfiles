FROM almalinux:9
RUN useradd expense
USER expense
CMD ["sleep","100"]


# by adding above code, we are just giving the user access(for whoever get into container using exec) but not the root access, which helps in security by protecting underlying hardware.
# this restricts user from downloading anything on container since user will not be having sudo access.
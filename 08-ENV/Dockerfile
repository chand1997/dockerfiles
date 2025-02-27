FROM nginx:latest
ENV password="password123"\
    email="chan@gmail.com"

# environment variables that can be accessed within image/container and they can be ovverridden during run using -e
# i.e docker run -e password=otherpassword

# we can see env variables using "docker inspect" 
# or 
# if we are inside container,we can see env variables by typing "env".
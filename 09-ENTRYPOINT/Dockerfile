FROM almalinux:9
# CMD ["ping","google.com"]

# if we are using just above code,we can override the above
# i.e "docker run <image-name>:<tag> ping facebook.com"

# ENTRYPOINT ["ping","google.com"]
# if we are using ENTRYPOINT instead of CMD, we cannot ovveride
# instead both command append (ping google.com ping facebook.com)and give error 


# for best usecase, we should use them together, i.e
CMD ["google.com"] 
ENTRYPOINT ["ping"]
# i.e "docker run <image-name>:<tag> facebook.com"






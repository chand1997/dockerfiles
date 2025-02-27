FROM nginx:latest
LABEL project="expense"\
      environment="dev"\
      version="v1"

# label is to add information about image,and to filter image
# we can filter image using labels ==> docker images -f "LABEL=project=expense"
# multiple filters ==> docker images -f "LABEL=project=expense" -f "LABEL=version=v1"  ...

# we can see these labels using ==> 
# "docker inspect <image-name>:<tag>/<container-name>/image-id/container-id"
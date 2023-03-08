https://phoenixnap.com/kb/how-to-commit-changes-to-docker-image
  
  
  How to use the Docker Build without reusing previous cached images: --no-cache (takes longer to build from scratch).
  ```
  docker build . -f Dockerfile \
    --network=host \
    --no-cache \
    
  ```
  
  
  Find docker images with tag and image id
  ```
  docker images
  ```
  run interactive container from image:
  ```
  docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
  docker run --name mycontainer -it IMAGE_ID
  docker run --name mycontainer -v /nfs:/nfs -it 97b9705c45ec
  exit 13
  ```
  find excited container id:
  ```
  docker ps
  ```
  if containe not present, look at all containers (stopped and excited),
  The docker ps command only shows running containers by default. To see all containers, use the --all (or -a) flag:
  ```
  docker ps -a
  ```
  start container if your container is not running.
  ```
  docker start mycontianer
  ```
  Next, execute an interactive sh shell on the container.
  ```
  docker exec [OPTIONS] CONTAINER COMMAND [ARG...]
  docker exec -it mycontainer sh
  ```
  run commands in your container and make some changes before exit.
  ```
  python setup.py build develop
  exit 13
  ```
  create an new image from a running container and assign a new name to your image.
  ```
  docker ps
  docker commit [CONTAINER_ID] [REPOSITORY[:TAG]]
  ```
  To push an image to a private registry and not the central Docker registry you must tag it with the registry hostname and port (if needed).
  ```
  docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
  docker tag 0e5574283393 myregistryhost:5000/fedora/httpd:version1.0
  ```
  Push to the dockerhub.
  ```
  docker push aicregistry:5000/${USER}:sf-base
  ```
  Check your images in the hub.
  ```
  docker images | grep mboels
  ```
  
  

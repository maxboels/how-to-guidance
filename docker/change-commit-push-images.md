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
  start interactive session with container from image:
  ```
  docker run -it [IMAGE_ID] bin/bash
  ```
  or use docker run and exec
  ```
  docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
  docker exec [OPTIONS] CONTAINER COMMAND [ARG...]
  ```
  
  ```
  python setup.py build develop
  exit
  ```
  The docker ps command only shows running containers by default. To see all containers, use the --all (or -a) flag:
  ```
  docker ps -a
  ```

  ```
  docker commit [CONTAINER_ID] [REPOSITORY[:TAG]]
  ```
  
  To push an image to a private registry and not the central Docker registry you must tag it with the registry hostname and port (if needed).
  ```
  docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
  docker tag 0e5574283393 myregistryhost:5000/fedora/httpd:version1.0
  ```
  
  
  ```
  docker push aicregistry:5000/${USER}:sf-base
  ```
  
  
  ```
  docker images | grep mboels
  ```
  
  

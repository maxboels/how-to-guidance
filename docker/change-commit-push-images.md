https://phoenixnap.com/kb/how-to-commit-changes-to-docker-image

  ```
  docker images
  ```
  
  ```
  start interactive session with container from image:
  docker run -it [IMAGE_ID] bin/bash
  ```
  
  ```
  python setup.py build develop
  exit
  ```
  
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
  
  

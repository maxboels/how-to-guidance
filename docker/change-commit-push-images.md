https://phoenixnap.com/kb/how-to-commit-changes-to-docker-image

  ```
  docker images
  ```
  
  ```
  docker run -it [IMAGE_ID] bin/bash
  ```
  
  ```
  python setup.py build develop
  exit
  ```
  
  ```
  docker ps -a
  ```
  docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]
  ```
  docker commit [CONTAINER_ID] [new_image_name]
  ```
  
  
  ```
  docker push aicregistry:5000/${USER}:sf-base
  ```
  
  
  ```
  docker images | grep mboels
  ```
  
  

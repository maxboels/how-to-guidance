https://phoenixnap.com/kb/how-to-commit-changes-to-docker-image

  ```
  docker images
  ```
  
  ```
  docker run -it cf0f3ca922e0 bin/bash
  ```
  
  ```
  python setup.py build develop
  exit
  ```
  
  ```
  docker ps -a
  ```
  
  ```
  docker commit [CONTAINER_ID] [new_image_name]
  ```
  
  ```
  docker images | grep mboels
  ```
  
  

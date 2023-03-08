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
  
  
  ```
  docker push aicregistry:5000/${USER}:sf-base
  ```
  
  
  ```
  docker images | grep mboels
  ```
  
  

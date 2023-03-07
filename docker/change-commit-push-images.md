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
  
  ```
  docker commit [CONTAINER_ID] [new_image_name]
  ```
  
  
  ```
  docker push registry-host:5000/myadmin/rhel-httpd:latest
  ```
  
  
  ```
  docker images | grep mboels
  ```
  
  

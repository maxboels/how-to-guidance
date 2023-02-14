Description
-----------

- Develop your projects in containered environments with docker. 
- Access containers with ssh to work on remote servers (mount your local machine in your container).


Install a Docker environment
---------------------------------
   
    
2. Install Docker:
    ```
    $ sudo apt update
    $ sudo apt install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
    ```

3. Install portainer:
	```
	$ docker volume create portainer_data
	$ docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest


4. Portainer web app GUI:
	```
	https://localhost:9443
	```
	
	```
	- create container:
		- Name: dev1
		- Image: pytorch/pytorch:latest
		- Advanced container settings:
			- Command & logging: select Interactive & TTY
			- Volumes: container: /home/mboels  (Bind) -> host: /home/mboels (Writable)
			- Restart policy: Always
			- Runtime & Resources: Runtime: nvidia
	```
	

6. Container ID:
	```
	$ docker ps
	```
			

4. Enter container (run locally):
	```
	$ docker exec -it dev1 /bin/bash
	$ docker exec -it <CONTAINER ID> /bin/bash
	```

7. change permission in container (remote server):
	```
	$ adduser mboels
	$ apt update
	$ apt install vim
	```
5. Find your local user id:
	```
	$ id
	```
	then on the remote server, change the userid to your local userid in password and group:
	```
	$ vim /etc/passwd
	```
	add your username to sudo and users, and userid to your username:
	```
	$ vim /etc/group
	```
	install sudo:
	```
	$ apt install sudo
	```


6. Access container locally:
	run container (locally) with your username:
	```
	$ docker exec -it -u mboels dev1 /bin/bash
	```
	install ssh in server and start ssh connection:
	```
	$ sudo apt install openssh-server
	$ sudo /etc/init.d/ssh start
	```

7. ssh your docker container from your local machine:
	```
	ssh mboels@172.17.0.4


8. Optional: create a config file to remove the username@IPaddress:

	```
	$ ssh-keygen -f "/home/mboels/.ssh/known_hosts" -R "172.17.0.3"
	$ docker commit dev mboels/pytorch:version1
	$ ssh dev1
	```


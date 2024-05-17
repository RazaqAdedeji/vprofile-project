## Prerequisites
- JDK 1.8 or later
- Maven 3 or later
- MySQL 5.6 or later
######
## Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- MySQL
## Database
Here,we used Mysql DB 
MSQL DB Installation Steps for Linux ubuntu 14.04:
- $ sudo apt-get update
- $ sudo apt-get install mysql-server

Then look for the file :
- /src/main/resources/accountsdb
- accountsdb.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < accountsdb.sql

##############

1. I made user use on Vagrant for this project. 
2. I used ubuntu OS on the vagrant
3. Then I install docker engine, after the installation I added vagrant into the Group name and the User Vagrant, with "usermod -aG docker vagrant", and you can confirm with "id vagrant", you see the group name and user added. 

4. Clone the source code and check out the branch "CONTAINER".
5. Write the Dockerfile for the app, db and web(nginx).
6. Go to dockerhub and create 3 new repository, named vprofileapp, vprofileweb, and vprofiledb
7. The repo is what I'm using to create the image tag in my docker compose file.
8. Then write a Docker compose file. Since the configuration for RabbitMQ and Memcached were easy, I just needed to push them from dockerhub. This is included in the Docker compose file and save.
9. cd into vagrant, then cd into vprofile-project, and build the docker compose file with "Docker compose build" or "docker compose up -d", this force all the container to build.
10. After all the containers are up and running, copy the IP of the vagrant "ip addr show" and put on the browser, you should see your application running.
11. Now push your images into your dockerhub. "docker login", then "docker push <image name>"
12. to view the dockerfile and the docker compose file, check the repo and switch to branch CONTAINER.
13. docker system prune -a" to format/delete all docker resource on your vm/server/local machine.

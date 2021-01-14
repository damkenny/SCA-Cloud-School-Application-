# SCA-Cloud-School-Application-

Tools used: Docker,Nginx VisualStudioCode, Git, Github.

Step 1. Creating a Directory for the Webpage


 A repository was created and cloned into visualstudio code which create a directory 
on my PC which include the landing page index.html file, an html file to display "Welcome to SCA Cloud School Application" 
and a docker file with the following command" 
FROM nginx:alpine
COPY . /usr/share/nginx/html " which was copying the content (images) of the directory into the container.

The docker desktop has to be running before the docker file can be created.


Step 2. Creating the image

The below command was use to create an image which was runned and tested in a container.
cmd  -- docker build . -t kehindeafusat/adeniye:finalImage. 
cmd -- docker images -- was used to check for the images created.


Step 3. Testing the image and running  the docker container.

The command -- docker container ls-- was used to check if there are any container 
running and docker container stop <container ID> (to stop the container running on a port)
using the port 80 or port 8080 to display the webpage with the text "Welcome to SCA Cloud School Application".

The command used to run the container was -- docker container run -p 80:80 kehindeafusat/adeniye:finalImages.
(The first 80 is the port docker is running on the second 
80 is the local port to run a container on port 80 which is repository name is adeniye and tag is finalImages)

Output:
 docker container run -p 8080:80 kehindeafusat/adeniye:finalImage
/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
/docker-entrypoint.sh: Configuration complete; ready for start up

 link to my application running 
 
 http://127.0.0.1/kennypage.html	
 
 http://localhost/
 
 http://localhost/8080

Step 4. Pushing the images to the docker container.

In the dockerhub, a repository called kehindeafusat/adeniye was created to allow the pushing of images from the container to docker
using the command -- docker push kehindeafusat/adeniye:finalImage

link to my dockerhub: https://hub.docker.com/repository/docker/kehindeafusat/adeniye


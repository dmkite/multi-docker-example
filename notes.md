# docker images
- file system - includes all executables 
- start command
When run it creates an image, copies file system, runs start command. Running system. Image allows many containers to be created (think imgage = class, container = object or instance). A template that produces a container once run.
# docker containers
- an image that has been run

`sudo docker ps -all` -> see all containers, including stopped. 

stopping and starting a container is useful because the filesystem persists. 

`docker build .` > image > container
`docker run` > container

every step of build creates a hash that is cached and later used if the image is rebuilt.

-t (tagged) flag allows a name
-d (detached mode) returns the command line. you must run docker kill to end it
exec -it (interactive, tty) enter a container file path
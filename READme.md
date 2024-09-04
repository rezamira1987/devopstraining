docker run --interactive --tty --rm ubuntu:22.04
root@938091c5f519
after running above docker image, ping not work, to resolve: 
install ping:
<!-- apt update
apt install iputils-ping -->

# exit from above container and using first command (line-1) can cause to remove all things that we installed.

# exit and run again first line command:
root@2b2b7398facd

# --rm
this flag cause to remove container after exitting from that container, if we want to keep the container, we should use --name flag instead.

## reza@ubuntu-std:~/git$ sudo docker ps -a
<!-- CONTAINER ID   IMAGE          COMMAND       CREATED          STATUS                     PORTS     NAMES
dc5886d4f9b1   ubuntu:22.04   "/bin/bash"   37 seconds ago   Exited (0) 4 seconds ago             my_ubuntu_container -->
as you can see above, after removing --rm and adding --name instead, the container will be kept. 


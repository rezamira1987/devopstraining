### 1. **Docker preview**

- **using a docker image**
  - docker run --interactive --tty --rm ubuntu:22.04
    ```markdown
        root@938091c5f519
  - after running above docker image, ping not work, to resolve: 
  - install ping:
     ```markdown
     apt update
     apt install iputils-ping

  - exitting from above container and using first command again, can cause to remove all things that be installed, also the image name will change
     ```markdown
     root@2b2b7398facd

  - rm flag (--rm):
     - this flag cause to remove container after exitting from that container, if we want to keep the container, we should use --name flag instead.
     ```markdown
      docker run --interactive --tty --name my_ubuntu ubuntu:22.04
      reza@ubuntu-std:~/git$ sudo docker ps -a
      CONTAINER ID   IMAGE          COMMAND       CREATED          STATUS                     PORTS     NAMES
      dc5886d4f9b1   ubuntu:22.04   "/bin/bash"   37 seconds ago   Exited (0) 4 seconds ago             my_ubuntu_container

  - as you can see above, after removing --rm and adding --name instead, the container will be kept. 
  - now, we can start it again and connect to it for the second time with all apt that be installed in the first time.
    ```markdown
      docker start my_ubuntu_container
      docker attach my_ubuntu_container
 
  - after above commands, we can go to the docker state that we left before, i mean ping is available on the docker
 




### 4. **Preview and Edit the Markdown:**

- **Visual Studio Code:**
  - Use the built-in Markdown preview by pressing `Ctrl + Shift + V` (or `Cmd + Shift + V` on Mac). You can also open the preview pane by right-clicking the `README.md` file and selecting **Open Preview**.
  
- **Visual Studio:**
  - Visual Studio doesn’t have a built-in Markdown preview, so you may want to use an external tool or online Markdown editor for previewing.

### 5. **Add Visual Enhancements:**

- Use **badges** (like build status, license, etc.) for visual enhancement. You can generate badges from sites like [Shields.io](https://shields.io).
- Add **screenshots or GIFs** to make your README more visually appealing. To do this, you can use the following Markdown syntax:

  ```markdown
  ![Screenshot](https://path/to/screenshot.png)
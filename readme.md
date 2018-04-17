# Docker Installation Guide

1. Install Docker for Windwos Community Edition from [Docker Hub Store](https://store.docker.com/editions/community/docker-ce-desktop-windows).
2. Once Docker configures all its setting, **right click** on **docker icon** from system tray and make sure you are running a **linux container**
    * If docker is running with windows container, option that says `swaitch to linux conatiner` will be availble
3. Open powershell in **adminstrator mode** and check `docker -v` to check docker is working
    * `Docker version 18.03.0-ce, build 0520e24` as of 04/16/2018
4. Run the app in local: run `npm install` then `npm start` and check on [localhost:3000](http://localhost:3000).
5. Build node-express image:
    * Run `docker build -t <your name>/node-express .`
    * Run `docker images` then you will see your app created 
    * To run the image run `docker run -p 3000:3000 -d <your name>/node-express`
    * Run `docker ps` to chekc if the container is running properly
6. To get into bash of your contianer run `docker exec -it <container id> /bin/bash`
7. You can call your app using curl inside the continaer by calling `curl -i localhost:3000`
    * if it says curl is missing, then install via `sudo apt-get install curl`# testingserver

# Wordpress docker boilerplate

Inspired by and based on (understand : copied/pasted from) Wodby images and WordPress stack, fine tuned to match my needs. Basically :

- Added a phpmyadmin image
- removed a whole lot of images that were of no use for me

Most of the credit goes to the [wodby crew](https://wodby.com/), who does an amazing job with those fantastic docker images. Give them some love, they deserve it

### How to use it ?

1. Install docker on your OS ([Mac](https://docs.docker.com/docker-for-mac/install/), [Linux](https://docs.docker.com/install/), [Windows](https://docs.docker.com/docker-for-windows/install/))
2. [Install docker-compose](https://docs.docker.com/compose/install/) 
3. clone this repository
4. copy/clone/unzip a wordpress into a folder name WordPress (that is very much WIP, see below)
5. fill the `.env` file with the information required (keep in mind that database name or user can be anything. If you plan of deploying the app live, you might want to think twice before using `toto` as DB_USER and `pooplol` as DB_ROOT_PASSWORD)
6. run `docker-compose up -d`, which may take a while if you need to download all the images and you have a crappy ADSL like I do
7. navigate to the url you specified in `.env` (`PROJECT_BASE_URL=whatever.docker.localhost`). You may change the domain as you please. Bear in mind that some won't work (such as `.lan`, `.dev`, `.local`)
8. And ... Voilà ! 

The php container is mapped with the WordPress folder, so you can add your themes or plugin locally, and they will be usable on your site.

### Any problem ?

- Do not hesitate to report it. Keep in mind that this is a self-learning project, so I do not promise any result or response time
- This is very much WIP, so do not hesitate to check often.
- If your issue is not resolved fast enough for you, fork at will !



### What's planned ?

This is pretty much WIP : this is a pet-project of mine to better understand and work with docker and devOps methodology. So, I plan on

 - adding a **_Makefile_** to kickstart wordpress projects, and do the same for Drupal 8 project (and pretty much any framework that I will fancy at a given time).
 - Add useful documentation on how to use this. This is actually the highest priority, to be honest
 - Fix the way the mapping is handled (i.e: include a make setup command that will git clone a clean wordpress in a {PROJECT_NAME} folder, rather than having to clone it manually in a WordPress folder)

---
This is **_my baby_** . I know he is probably broken and messed up but I love it the way it is. But please, fill issues, comments, forks if you want to ! :P

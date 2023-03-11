# wordpress-docker
Quickly setup a Wordpress installation using docker-compose.

# Prerequisites
1. Install [Docker](https://docs.docker.com/engine/install/)
2. Install [docker compose](https://docs.docker.com/compose/install/)

# How to run
To run Wordpress locally all you have to do is run the ```docker compose up -d``` command. This will start up the Wordpress container, a MariaDB database and phpMyAdmin for managing the database. 

# Develop a custom theme
After firing up Wordpress, a new directory will be created named ```wp-content``` which will contain the themes folder. In order to start developing a new theme all you have to do is create a new folder inside ```themes/``` with the name of your theme and create all the [necessary files](https://codex.wordpress.org/Theme_Development) for the theme to work.

**Notice**: If you're trying to build a new Wordpress theme on Linux you need to create your theme's folder using sudo, because the ```themes/``` directory is owned by a different user. You can then change the ownership of your theme's folder with ```chown -R 1000:1000 <theme-folder-path>``` to avoid using sudo on every file change.

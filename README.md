# Nextcloud on Docker with Face Recognition and Cron
This Dockerfile extends the official nextcloud:apache Dockerfile (https://hub.docker.com/_/nextcloud) with Face Recognition Capabilities in your Nextcloud images. Additionally this Dockerfile add cron via supervisory.

After installation please install the Nextcloud App from https://apps.nextcloud.com/apps/facerecognition. Please activate the app after the installation. The Cronjob will soon start and will try to detect all faces within your pictures.

# Installation
In general, follow the instructions on https://hub.docker.com/_/nextcloud to use this image. Especially please check out the environment variables to configure your nextcloud docker installation.

# Post installation configuration

1. Install Face Recognition App
Please access your nextcloud installation in your favorite browser to install and enable the face recognition app (https://apps.nextcloud.com/apps/facerecognition).

2. Activate the Cron
Activate the cron scheduler, which is part of the image. Go to Settings -> Basic Settings and select the option "Cron" for the Background jobs. That's make the web interface more responsive, especially with a lot of files or if you have many users. Background jobs are executed every 5 minutes.

![Cron Scheduler](https://github.com/iamklaus/nextcloud/raw/main/images/cron.gif | width="100%") 
<!-- .element width="100%" -->

# Environment variables

MEMORY_LIMIT
Please configure the environment variable MEMORY_LIMIT (https://www.php.net/manual/en/ini.core.php#ini.memory-limit). The default value is 1 GByte. If you can add more, please do so.

NEXTCLOUD_UPDATE
Set NEXTCLOUD_UPDATE to "1" if you want to receive updates.

# More
Follow my blog to receive the latest information: https://iamklaus.org/category/nextcloud/

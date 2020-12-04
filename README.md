# Nextcloud on Docker with Face Recognition and Cron
This Dockerfile extends the official nextcloud:apache Dockerfile (https://hub.docker.com/_/nextcloud) with Face Recognition Capabilities in your Nextcloud images. Additionally this Dockerfile add cron via supervisory.

After installation please install the Nextcloud App from https://apps.nextcloud.com/apps/facerecognition. Please activate the app after the installation. The Cronjob will soon start and will try to detect all faces within your pictures.

# Installation
In general, follow the instructions on https://hub.docker.com/_/nextcloud to use this image. Especially please check out the environment variables to configure your nextcloud docker installation.

# Post installation configuration
Please access your nextcloud installation in your favorite browser to install and enable the face recognition app (https://apps.nextcloud.com/apps/facerecognition).

I recommend activate the cron scheduler, which is part of the image. Go to Settings -> Basic Settings and select the option "Cron" for the Background jobs. That's make the web interface more responsive, especially with a lot of files or if you have many users. Background jobs are executed every 5 minutes.

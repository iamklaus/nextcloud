# Nextcloud on Docker with Face Recognition and Cron
This Dockerfile extends the official nextcloud:apache Dockerfile (https://hub.docker.com/_/nextcloud) with Face Recognition Capabilities in your Nextcloud images. Additionally this Dockerfile add cron via supervisory.

After installation please install the Nextcloud App from https://apps.nextcloud.com/apps/facerecognition. Please activate the app after the installation. The Cronjob will soon start and will try to detect all faces within your pictures.

# How to use it?
In general, follow the instructions on https://hub.docker.com/_/nextcloud to use this image. Especially please check out the environment variables to configure your nextcloud docker installation.

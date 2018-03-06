# Starbelly: Crawl Me

This repo contains a dummy website for testing a web crawler such as Starbelly.
The dummy site is hosted by nginx and it contains a small number of pages and
images.

You can run this inside a docker container as follows:

    docker run --rm --name crawlme --network starbellydev_default \
               -v $PWD:/usr/share/nginx/html nginx:latest

Note that this command will attach the dummy site to the `starbelly-dev`
network, which is appropriate for developers. If you want to connect to a
production setup, change the network to `starbelly_default`.

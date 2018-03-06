# Starbelly: Crawl Me

This repo contains a dummy website for testing a web crawler such as Starbelly.
The dummy site is hosted by nginx and it contains a small number of pages and
images.

You can run this inside a docker container as follows:

    docker run --rm --name crawlme --network starbellydev_default \
               -v $PWD/www:/usr/share/nginx/html nginx:latest

Note that this command will attach the dummy site to the `starbelly-dev`
network, which is appropriate for developers. If you want to connect to a
production setup, change the network to `starbelly_default`.

To crawl this site with Starbelly, use the URL `http://crawlme`. Note: due to
the way Docker handles domain names, you will not be able to access this URL
from the host machine, but it will resolve correctly from a Starbelly instance.
If you wish to connect from your host, you can specify a port, i.e. add the flag
`-p 127.0.0.1:10080:80` to the Docker command above, and then you can access the
dummy site from your host using the URL http://127.0.0.1:10080.

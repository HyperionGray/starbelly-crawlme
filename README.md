# Starbelly: Crawl Me

This repo contains a dummy website for testing a web crawler such as Starbelly.
The dummy site is hosted by nginx and it contains a small number of pages and
images.

You can run this inside a docker container as follows:

    $ docker run \
        --rm --name crawlme -p 127.0.0.1:10080:80 \
        -v $PWD/www:/usr/share/nginx/html nginx:latest

To crawl this site with Starbelly, use the URL `http://localhost:10800`.

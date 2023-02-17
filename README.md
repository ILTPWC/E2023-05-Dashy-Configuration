# ILTPWC - My Dashy Configuration

Hey guys in this repository you will find my dashy dashboard configuration as well as my traefik and docker-compose config to setup dashy with SSL certificates with letsencrypt.

The configuration belongs to the following YouTube Video: https://www.youtube.com/watch?v=DBnMGrHROBg

In order to run the docker-compose file you need to adjust the traefik configuration first and replace the <VARIABLES> with your credentials.

You also need to add the external docker network manual with docker network create iltpw

After that just use docker-compose up -d to the services on your docker host (-d is to detach the script from your shell so that in runs in background)



Traefik is configured with Basic Auth user:pass is iltpwc - you can change that in the dynamic.yml of traefik - Hint: google for htauth generator to create the string

My letsencrypt dns provider for the ssl certificate is digitalocean but you can change that to what ever provide you use


In order to create a system dashboard with dashy you should have a look on glances which is the linux service that I use to collect the data from the server - it's like htop/top but with a REST API build in.


If you like what I am doing please consider to like and subscribe to https://www.youtube.com/@ILTPWC - it makes a whole lot of a different for me
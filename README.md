# guru

requirements:

Write down a valid docker-compose.yml (in version 3.2) config file which contains:

3 services (web, sidekiq and crono)
Each of these services must work with “docker deploy” command (be possible to deploy it to Swarm)
Each of these services should have a memory limit of 800Mb and CPU set to 0.25
Docker image for each service should be quay.io/netguru/baseimage:0.10.2
“Web” service should have attached to volumes:
staging-assets:/app/public/assets
/var/log/app:/app/log
Service “web” and “sidekiq” use a “swarm” network which is external
Service “sidekiq” and “crono” use “internal” network
command: can be anything

How to start:
docker stack deploy --compose-file /path/to/docker-compose.yml <stack name>

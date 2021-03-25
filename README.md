# fail2ban
Fail2ban service for docker host based on Alpine Linux

## Quick Start
command:

    docker run -d --cap-add=NET_ADMIN --network=host --name fail2ban zeaq/docker-fail2ban

## docker-compose
docker-compose.yml:

    firewall:
        image: zeaq/docker-fail2ban
        restart: always
        cap_add:
            - NET_ADMIN
        network_mode: host

## Build
commands:

    docker build docker-fail2ban -t fail2ban
    docker run -d --cap-add=NET_ADMIN --network=host --name fail2ban fail2ban


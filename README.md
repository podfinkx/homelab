# Homelab setup

This repo is for documenting my homelab setup, It will consist of a series of bash scripts, ansible playbooks and docker-compose files.

>*Feel free to grab what you need. 🍻*

## Table of Contents
  1. [Docker](#docker)

## Docker

My docker setup is pretty simple one global docker-compose.yml file and every container that needs his own config on a separate folder.

> *I say every container that need his own config because not all of them need a directory on this structure, for example pihole is declared inside docker-compose.yml but there is not need to create a folder inside this structure for him. The pihole config files resides on an external folder that is constantly backed up via borg backup.*

Example structure:

    traefik/
    traefik/dynamic.toml
    traefik/traefik.toml
    .env
    docker-compose.yml

>*You can read more about my complete docker setup [here](docker/)*

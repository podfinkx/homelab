# My Docker Setup

My docker setup hosts most of my services that are essential for my daily use.

* Services:
    ```
    # utils
    watchtower  # auto updates for all containers

    # network
    traefik     # reverse proxy
    pihole      # dns level adblocker

    # media
    *jackett     # API Support for your favorite torrent trackers
    *jellyfin    # media system
    *radarr      # A fork of Sonarr to work with movies
    *sonarr      # Smart PVR for newsgroup and bittorrent users
    *deluge      # BitTorrent client
    *jdownloader # Download manager 

    note: services marked with a * are yet to be implemented.
    ```
    *the global docker-compose.yml file follows this exact order*

## Traefik

For traefik you will need to create two files:
* acme.json (this file stores the letsencrypt certificate and needs chmod 600) 
* authFile

```
touch traefik/{acme.json,authFile}
chmod 600 traefik/acme.json
```
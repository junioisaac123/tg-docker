# TG Docker Project Struct

This is the tg project docker struct with containers using:

- mysql
- php-fpm
- nginx

## Dir project

```bash
/.
 ├── containers/ # Struct to containers
 │  ├── db/ # Database
 │  ├── logs/ # Logs for nginx in accesed logs and errors
 │  ├── nginx/
 │  │  └── templates/
 │  │     └── default.conf.template # Nginx template
 │  └── php-fpm/
 │     └── Dockerfile # Build container in php-fpm configs + laravel
 ├── laravel-app/ # Laravel project
 ├── docker-compose.yml # Struct for project compose containers
 └── README.md
```

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

## Run

Clone the actual project

```bash
git clone https://github.com/junioisaac123/tg-docker
```

Go inside the folder

```bash
cd tg-docker
```

Clone the laravel project to `laravel-app`

```bash
git clone https://github.com/junioisaac123/tg-2024 laravel-app
```

Run the docker build

```bash
docker compose up -d --build
```

### Stop

```bash
docker compose down
```

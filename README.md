# Docker Multiple PHP
Docker enviroment for multiple php application development. It can run multiple php version at a time. It consists of the following:
- PHP 7.4 & PHP 8.2
- Apache
- MariaDB
- PostgreSQL
- Composer

## Setup
Clone or download this repository and run
```bash
docker compose up
```

## Directory Structure
    ├── docker-files                   # Dockerfiles for php
        ├── PHP74.Dockerfile           # Dockerfile for php7.4
        ├── PHP82.Dockerfile           # Dockerfile for php8.2
    ├── mariadb-data                   # MariaDB Server Data
    ├── pgsql-data                     # PostgeSQL Server Data
    ├── www                            # Docker volume for /var/www/html/
        ├── php74                      # Docker volume for /var/www/html/ php7.4
        ├── php82                      # Docker volume for /var/www/html/ php8.2
    ├── docker-compose.yaml            # Docker compose file

## Usage
After running docker compose up put your php application file into www/php{version}. php apache server will run on port 8074, 8082
| Container | Port   |
| :-------- | :----- |
| `PHP 7.4` | `8074` |
| `PHP 8.2` | `8082` |
| `MariaDB` | `3300` |

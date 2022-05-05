# Gitea Docker Compose 

This repo contains a docker-compose file to set up a <a href="https://gitea.io/en-us/">gitea</a> container with a <a href="https://www.postgresql.org/">postgres</a> database. Gitea is a open source lightweight code hosting solution.

## Requirements 

- docker https://docs.docker.com/engine/install/

- docker-compose https://docs.docker.com/compose/install/

## Usage 

##### Clone this repository: 

` $git clone https://github.com/mert-il/gitea-docker.git `

##### Copy .env.example as .env:

` $cp .env.example .env `

##### Edit .env file:

Change the values as required

```
USER=gitea
USER_UID=1000
USER_GID=1000
GITEA_PORT=3000
GITEA_SSH_PORT=222
POSTGRES_USER=gitea
POSTGRES_PASSWORD=gitea
POSTGRES_DB=gitea
PORTGRES_PORT=5432
``` 

##### Run docker compose:

` $docker-compose up -d --build `

##### Open gitea in the browser:

Enter ` http://localhost:gitea_port ` or ` http://your_ip:gitea_port  `

## Setup

Next, an initial configuration window opens. This normally does not need to be changed as it takes the data from the .env file. However if you use it publicly you have to change the URL for <strong>Gitea-Basis-URL</strong>. In addition, you can create an admin account under optional settings. Next install gitea.

Now create your first account or log in with the admin account if you have created it bevore.

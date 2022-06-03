# SQL Server

## Usage

Make a directory on your Docker server for this program and copy the `docker-compose.yml` and `.env` files to it. Additionally, you may wish to copy the `docker-compose.override.yml` file from one of the three folders in this repository accordingly:

- network  
if you want to specify the name of the Docker network that SQL Server will create. Otherwise, the default name generated by Docker Compose will be used.
- port  
if you want to specify a port to use. Otherwise, no external port will be used.
- network-and-port  
to combine the above two options.

## Settings

- DB_PASSWORD  
The password of the SA account of SQL Server. This is required.
- VOLUME  
The name of the Docker volume used to persist SQL Server's data. This is required.
- NETWORK  
The name of the Docker network to create. This is required if the `network` or `network-and-port` override file is used.
- PORT  
The port to use, using Docker Compose short syntax, if the `port` or `network-and-port` override file is used. Defaults to `1433:1433` if not provided.

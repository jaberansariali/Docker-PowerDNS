# Docker-PowerDNS
This project includes PowerDNS as the local DNS records and Dnsdist as the DNS load balancer and MySQL as the database for the PowerDNS.

## Requirements

### Docker

To use this project you need docker daemon installed.

### Docker-compose

I suggest better build and run using docker-compose. you can download binary file [here](https://github.com/docker/compose/releases) then change the mode to executable. you can use this below.

```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose

sudo chmod +x /usr/bin/docker-compose
```

## Environment Variables on Docker-compose.yml

      - MYSQL_ROOT_PASSWORD=LJsa65d9DFxcvbrfTYzxcb
      - MYSQL_USER=powerdns
      - MYSQL_PASSWORD=powerdns
      - MYSQL_DATABASE=powerdns

These are used for MySQL login and create the database.

## Config Files

### dnsdist

This file contains all config files for the Dnsdist such as pool, server, ACL, action. for more information click [here](https://dnsdist.org/reference/config.html)

### powerdns

This file contains all config files for the PowerDNS and connection config file  to MySQL, for more information click [here](https://doc.powerdns.com/)

### mysql-data

This file contains the primary PowerDNS MySQL tables.

### Build and run 

You can simply run this command for build and run:

```
docker-compose up -d --build 

```
# Build a TOR Project SNOWFLAKE Proxy from source

## Build the image yourself from the git repository

```bash
$ git clone https://gitlab.torproject.org/tpo/anti-censorship/docker-snowflake-proxy
$ cd docker-snowflake-proxy
$ docker build -t snowflake-proxy .
$ sed -i 's/thetorproject\/snowflake-proxy:latest/snowflake-proxy/' docker-compose.yml
$ docker-compose up -d
```

## Check if docker is up and running
```bash
$ docker-compose ps
```
Example output:
```bash
     Name          Command     State   Ports
--------------------------------------------
snowflake-proxy   /bin/proxy   Up           
```

## Check the logs
```bash
$ docker-compose logs -f snowflake-proxy
```
Example output:
```bash
snowflake-proxy    | 2022/03/05 05:23:12 In the last 1h0m0s, there are 3 connections. Traffic Relayed ↑ 336 MB, ↓ 336 MB.
snowflake-proxy    | 2022/03/05 06:23:12 In the last 1h0m0s, there are 3 connections. Traffic Relayed ↑ 25 MB, ↓ 25 MB.
snowflake-proxy    | 2022/03/05 07:23:12 In the last 1h0m0s, there are 2 connections. Traffic Relayed ↑ 206 MB, ↓ 206 MB.
snowflake-proxy    | 2022/03/05 08:23:12 In the last 1h0m0s, there are 2 connections. Traffic Relayed ↑ 454 KB, ↓ 454 KB.
```

## Project site
https://snowflake.torproject.org/
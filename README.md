# go_http_api_template
go web api server environment template.

## Features
- golang:1.15.12
- air
- mysql:5.7
- phpmyadmin

## Quick Start
copy env  
$ `cp .env.example .env`  
change db name on .env and docker-compose.yml  
build docker image  
$ `docker-compose build`  
make container of web(go), mysql, phpmyadmin  
$ `docker-compose up -d`  
check server logs  
$ `make logs`  
enter the web container   
$ `make web`  
migration  
\# `goose up`

access web  
http://localhost:8080/  
access phpmyadmin  
http://localhost:8081/

## Tips
- You don't need to run `go run main.go` everytime you changed go file. [Air](https://github.com/cosmtrek/air) is running in go_web container

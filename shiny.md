# Docker

#### Installation of Docker (Ubuntu 14.04)

```
apt-get update
apt-get -y install docker.io
```
```
docker run -help
```
#### Docker for Shiny Server
```
docker run --rm -p 3838:3838 rocker/shiny
```

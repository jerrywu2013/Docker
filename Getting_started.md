# Docker

#### Installation of Docker (Ubuntu 14.04)
```
apt-get update
apt-get -y install docker.io
```
1.Pull image
```
docker pull
sudo docker pull ubuntu:14.04
```
2.List image
```
sudo docker ps -a
```

3.Run image
```
sudo docker run -t -i ubuntu:14.04 /bin/bash
```

4.Create new image
```
sudo docker run -t -i ubuntu:14.04 /bin/bash
sudo docker commit -m "NEW" -a "Docker Newbee" "your ID" ubuntu:14.04:v2
```

5.Export and Import 
```
sudo docker export 6791a814380e > ubuntu.tar 
sudo docker load --input ubuntu_14.04.tar
```

6.Remove
````
docker ps -a -q 
docker rm
sudo docker rmi ubuntu:14.04
```


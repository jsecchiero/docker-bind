# docker-bind
A working bind service under alpine with docker

```bash
git clone https://github.com/jsecchiero/docker-bind.git
cd docker-bind
IMAGE=$( docker build . )
sudo docker run -d --name dns --publish 53:53/udp --publish 53:53/tcp -v /etc/dns:/etc/bind $IMAGE
```

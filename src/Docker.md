#Docker install on Raspberry Pi
```
sudo apt-get install -y apt-transport-https
```

sudo systemctl enable docker
```
sudo usermod -aG docker pi
```
You will need to logout and log back in for permission to take effect.

```
docker info
```

Get bash prompt inside container!
```
docker run -it dfoderick/fullcyclereact /bin/bash
```
docker run --name fullcycleapi-api -d --restart unless-stopped fullcycleapi

Get bash prompt inside container
```
docker run -it dfoderick/fullcyclereact /bin/bash
```

# Build for Docker:
git clone
docker login
cd fullcyclereact/
docker build -t fullcycle/web .
docker push fullcycle/web:latest

Install:
docker stop fullcycleapi fullcycleweb
docker rm fullcycleapi fullcycleweb

!don't think -i should be passed here
docker run --name fullcycleapi -d --network=host --restart unless-stopped fullcycle/api
docker run --name fullcycleweb -d --network=host --restart unless-stopped fullcycle/web

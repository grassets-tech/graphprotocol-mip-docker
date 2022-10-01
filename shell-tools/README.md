# Docker Image

`sudo docker build --no-cache -t davaymne/shell-tools:v0.19.3.0 .`


# Push image

`sudo docker push davaymne/shell-tools:v0.19.3.0 `


# How to use

```
sudo docker exec -ti shell-tools indexer connect http://indexer-agent:18000
sudo docker exec -ti shell-tools indexer status

```


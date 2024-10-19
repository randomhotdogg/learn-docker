### 安裝 docker

安裝 docker desktop 就可以使用 docker cli
https://www.docker.com/products/docker-desktop/

### docker image & container

image 類似 class
container 類似 instance

從一個 image 可以創建多個 container
每個 container 都是該 image 的獨立運行實例

### docker 指令

`docker version` 查看 docker 版本

`docker images` 查看目前的 images

`docker ps` 查看目前正在運行的 containers

- -a：查看目前所有的 containers，包含沒有在運行的

`docker pull {image_name}:{tag}` 下載指定版本的 image，沒帶上版本則預設使用 latest

`docker run {image_name}:{tag}` 使用指定版本的 image 執行 container

- -d or --detach：可以在背景運行
- -p or --publish {host_port} {container_port}：port binding
- --name {custom_name}：自己定義 container 的名字

`docker stop {container ID}` 停止 container

`docker start {container ID}` 再次啟動被停止的 container

`docker logs {container ID}` 輸出 container 執行 logs

### docker registry

### docker hub

docker 官方的 image 倉庫
https://hub.docker.com/

docker official images

軟體的版本對應到 docker hub 的 tag

### 私人倉庫

各家雲端都有提供：AWS ECR, GCP, Azure

### docker run 觀念

每次下 docker run 指令都會建立一個新的 container，不會使用舊的

### Dockerfile

建立 docker image 的說明書

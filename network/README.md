# Docker 网络

```console
docker network ls
```

* none 网络

>>docker run -it --network=none image
没有网络连接

* host 网络

>>连接到host网络的容器共享 docker host的网络栈，容器的网络配置与host完全一样。可以通过--network=host指定使用host网络。
docker host 容器对于网络传输有较高要求，则可以选择host网络，不便之处是牺牲灵活性，要考虑端口冲突的问题，dokerhost 上已经使用的端口就不能在使用


* bridge 网络

>>

* user-defined 网络

>> 
```console
docker network create --driver bridge my_network
```

```console
docker run -it --network=my_net busybox
```

```console
docker network connect my_net image_id
```
## 外部世界访问容器

答案是端口映射

```console
docker run -d -p 8080:80 httpd
```
将80端口映射到host的8080端口
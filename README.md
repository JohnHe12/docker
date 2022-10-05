# Docker

image container is different 

image can be create and can not be wrroten 

container can be read and wroten and the dockerfile can create the image and then  

use 
```console
docker build --pull -rm -f dockerfile_path -t image_name build_file
```

to create the image .

then use docker run -it 
or 
```console
docker run -d --name the_name_of_the_container ...
```  

use ***ctr D*** to exit the interface

use
 ```console
docker attach container
``` 
or 
```console
docker exec -it container bash
```

* can delete the container 

docker rm 

```console
docker rm $(docker ps -aq -f status=exited)
```
docker rmi delete the image

内存限制

```console
docker run -m 200M --memory-swap=300M ubuntu
```

cpu 限额

docker 可以通过 -c 或者 --cpu-share
通过 -c 设置的 cpu share 并不是绝对值他是占所有容器的权重，通过这个可以设置容器使用cpu的优先级


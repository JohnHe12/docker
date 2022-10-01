# Dockfile
## dockfile 的常用指令

* FROM 
>指定base的镜像

* MAINTAINER
>设置镜像的作者可以是任意的字符串

* COPY
>将文件从 build context 复制到镜像。
>COPY 支持两种形式： COPY src dest 与 COPY["src","dest"]。
注意： src只能指定build context 中的文件。

* ADD
>与COPY 类似，从 build context 复制文件到镜像。不同的是如果src是归档文件（tar,zip,tgz,xz等），文件会被自动解压到dest

* ENV
设置环境变量，环境变量可被后面的指令使用。例如:  
```console
ENV MY_VERSION 1.3 RUN APT-GET INSTALL -Y MYPACKAGE=$MY_VERSION
```

* EXPOSE
>指定容器中的进程会监听某个端口，Docker 可以将该端口暴露出来。

* VOLUME
>将文件或目录声明维volume。

* WORKDIR
>为后面的RUN,CMD,ENTRYPOINT,ADD或COPY指令设置镜像中的当前工作目录

* RUN
>在容器中运行指定的命令。

* CMD
>容器启动时运行指定的命令。Dockerfile 中可以有多个 CMD 命令，但是只有最后一个生效。 CMD 可以被 docker run 之后的参数替换

* ENTRYPOINT
>设置容器启动时运行的命令。Dockerfile 中可以有多个 ENTRYPOINT 指令，但是只有最后一个生效。 CMD 或 docker run 之后的参数会被当做采纳数传递给 ENTRYPOINT。
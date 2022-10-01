# RUN vs CMD vs ENTRYPOINT

(1) **RUN** : 执行命令并创建新的镜像层， RUN 经常用于安装软件包。
(2) **CMD** : 设置容器启动后默认执行的命令及其参数，但 CMD 能够被 docker run 后面跟的命令行参数替换。
(3) **ENTRYPOINT**  : 配置容器启动时运行的命令
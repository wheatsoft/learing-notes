# dockerfile说明

DockerFile

dockerfile使用说明文档[https://docs.docker.com/engine/reference/builder/](https://docs.docker.com/engine/reference/builder/)

```bash
# 基于的基础镜像
FROM ubuntu:14.04
# 维护者
MAINTAINER liyudong <1768756152@qq.com>

# 设置变量REFRESHED_AT为2014-06-01
ENV REFRESHED_AT 2014-06-01
RUN apt-get -yqq update
RUN apt-get -yqq install ruby ruby-dev make nodejs
RUN gem install --no-rdoc --no-ri jekyll -v 2.5.3
# 声明数据卷
VOLUME /data
VOLUME /var/www/html

# RUN, CMD, ENTRYPOINT的工作目录
WORKDIR /data
ENTRYPOINT [ "jekyll", "build", "--destination=/var/www/html" ]
```

RUN命令执行命令并创建新的镜像层，通常用于安装软件包

CMD命令设置容器启动后默认执行的命令及其参数，但CMD设置的命令能够被docker run命令后面的命令行参数替换

ENTRYPOINT配置容器启动时的执行命令（不会被忽略，一定会被执行，即使运行 docker run时指定了其他命令）


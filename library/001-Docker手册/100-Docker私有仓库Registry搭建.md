## Docker私有仓库Registry搭建 

官方镜像源：https://hub.docker.com/_/registry/  

```
docker pull registry
```

步骤：
1. 获取hub.docker上registry镜像(20170805当前最新版本是2.6.2)  
    docker pull registry:2.6.2



docker是一个非常好用的虚拟化工具。

下面给出建立私有docker hub的方法。docker将私有hub的环境打包在registry image中

执行指令：

docker run -p 5000:5000 registry

这条指令启动一个基于registry image的cotainer。并将host主机的port 5000绑定到虚拟机的端口5000。

这样，对该host主机端口5000的任何访问都转移到虚拟机中。

上传image：

首先给image赋予一个tag

docker tag $ID $IP:$port/$name

如  docker tag b832n2b87 192.168.1.1:5000/vim

ID为image的ID，IP为host主机的IP，name为该image的名字

docker push  192.168.1.1:5000/vim

下载image：

docker pull  192.168.1.1:5000/vim
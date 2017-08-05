## Docker私有仓库Registry搭建 

官方镜像源：https://hub.docker.com/_/registry/  

Github：https://github.com/docker/distribution-library-image.git


配置步骤：

1. 获取hub.docker上registry镜像(20170805当前最新版本是2.6.2)  https://hub.docker.com/_/registry/  
    ``` 
    docker pull registry:2.6.2 
    ```
2. 启动registry容器，挂载本地磁盘指定路径到容器中仓库存储路径
    
    默认配置信息：
    ```yaml
    version: 0.1
    log:
      fields:
        service: registry
    storage:
      cache:
        blobdescriptor: inmemory
      filesystem:
        rootdirectory: /var/lib/registry
    http:
      addr: :5000
      headers:
        X-Content-Type-Options: [nosniff]
    health:
      storagedriver:
        enabled: true
        interval: 10s
        threshold: 3
    ```
    配置信息可根据需要修改，根据Dockerfile文件可知config.yml文件位置，通过filesystem可以看出仓库存储路径。
    
    启动容器，映射端口50000到容器中registry端口5000，映射路径/home/docker/registry到容器/var/lib/registry，其他配置保持默认。
    ```
    docker run -d -p 5000:5000 --restart always --name registry -v E:/home/docker/registry:/var/lib/registry  registry:2.6.2   
    ```
    运行容器后，查看容器状态或浏览器查看地址：http://127.0.0.1:5000/v2/ ，返回json对象则表示启动成功。
    
    


先打标签再push  

上传image：

首先给image赋予一个tag

docker tag $ID $IP:$port/$name

如  docker tag b832n2b87 192.168.1.1:5000/vim

ID为image的ID，IP为host主机的IP，name为该image的名字

docker push  192.168.1.1:5000/vim

下载image：

docker pull  192.168.1.1:5000/vim


### 使用Dockerfile创建容器

```
# 创建Docker registry 服务


```
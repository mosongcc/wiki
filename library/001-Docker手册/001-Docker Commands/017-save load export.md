
## save export 区别


### save
save保存镜像到本地，镜像包含历史版本信息，可切换版本。
```
sudo docker save <IMAGE ID> > /home/save.tar
```

导入save.tar文件

    docker load < /home/save.tar


### export
export 保存容器到本地，不包含历史信息，无法切换版本。
```
sudo docker export <CONTAINER ID> > /home/export.tar
```
## docker info

Docker 信息查看命令。

## info命令
```
PS C:\Users\song> docker info --help
Usage:  docker info [OPTIONS]
显示整个系统的信息 
 
Options:
  -f, --format string   使用指定的Go模版对输出格式化
      --help            Print usage
```

## 使用示例

查看docker系统信息 
```
PS C:\Users\song> docker info
Containers: 0         #容器数量             
Running: 0            #运行中的容器             
Paused: 0             #暂停的容器
Stopped: 0            #停止的容器
Images: 0             #镜像数
Server Version: 17.06.0-ce
Storage Driver: overlay2
Backing Filesystem: extfs
Supports d_type: true
Native Overlay Diff: true
Logging Driver: json-file
Cgroup Driver: cgroupfs
Plugins:
Volume: local
Network: bridge host ipvlan macvlan null overlay
Log: awslogs fluentd gcplogs gelf journald json-file logentries splunk syslog
Swarm: inactive
Runtimes: runc
Default Runtime: runc
Init Binary: docker-init
containerd version: cfb82a876ecc11b5ca0977d1733adbe58599088a
runc version: 2d41c047c83e09a6d61d464906feb2a2f3c52aa4
init version: 949e6fa
Security Options:
seccomp
Profile: default
Kernel Version: 4.9.31-moby
Operating System: Alpine Linux v3.5
OSType: linux
Architecture: x86_64
CPUs: 2
Total Memory: 3.837GiB
Name: moby
ID: IMFZ:7SI7:5KG5:G7CK:P5IL:U3YK:QVBU:T6RD:6VUP:K7RV:P7EA:B2NJ
Docker Root Dir: /var/lib/docker
Debug Mode (client): false
Debug Mode (server): true
File Descriptors: 15
Goroutines: 24
System Time: 2017-07-01T09:41:30.8846736Z
EventsListeners: 0
Registry: https://index.docker.io/v1/
Experimental: true
Insecure Registries:127.0.0.0/8
Registry Mirrors:https://62oh.mirror.aliyunos.com/   #配置镜像地址
Live Restore Enabled: false
``` 




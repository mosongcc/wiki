

使用docker exec命令
这个命令使用exit命令后，不会退出后台，一般使用这个命令，使用方法如下

    docker exec -it db3 /bin/sh 或者 docker exec -it d48b21a7e439 /bin/sh
 
db3是后台容器的NAMES,d48b21a7e439是容器的进程ID  CONTAINER ID
 /bin/sh 是固定写法，它也能进入这个容器
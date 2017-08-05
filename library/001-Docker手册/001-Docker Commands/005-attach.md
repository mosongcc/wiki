
使用docker attach命令
    docker attach db3 或者 docker attach d48b21a7e439
 
db3是后台容器的NAMES,d48b21a7e439是容器的进程ID CONTAINER ID   然后就进去了这个容器的ssh界面。   
但是它有一个缺点，只要这个连接终止，或者使用了exit命令，容器就会退出后台运行

如何退出容器  

【场景一】如果要正常退出不关闭容器，请按Ctrl+P+Q进行退出容器。   
【场景二】如果使用exit退出，那么在退出容器后会关闭容器 
 
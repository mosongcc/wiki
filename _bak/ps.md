## docker ps 


### 命令参数
````
PS C:\Users\song> docker ps --help
Usage:  docker ps [OPTIONS]
List containers
Options:
  -a, --all             Show all containers (default shows just running)
  -f, --filter filter   Filter output based on conditions provided 根据所提供的条件过滤输出
      --format string   Pretty-print containers using a Go template
      --help            Print usage
  -n, --last int        Show n last created containers (includes all states) (default -1)
  -l, --latest          Show the latest created container (includes all states) 显示最新创建的容器(包括所有状态)
      --no-trunc        Don't truncate output 不截断输出
  -q, --quiet           Only display numeric IDs 只显示ID
  -s, --size            Display total file sizes   显示总文件大小
````

### 使用实例


```
PS C:\Users\song> docker ps -a
CONTAINER ID        IMAGE                 COMMAND                  CREATED             STATUS              PORTS               NAMES
cdf8ba098d77        nginx:1.13.0-alpine   "nginx -g 'daemon ..."   6 minutes ago       Up 6 minutes        80/tcp              nginx1.13.0
PS C:\Users\song> docker ps -l
CONTAINER ID        IMAGE                 COMMAND                  CREATED             STATUS              PORTS               NAMES
cdf8ba098d77        nginx:1.13.0-alpine   "nginx -g 'daemon ..."   6 minutes ago       Up 6 minutes        80/tcp              nginx1.13.0
PS C:\Users\song> docker ps -n 2
CONTAINER ID        IMAGE                 COMMAND                  CREATED             STATUS              PORTS               NAMES
cdf8ba098d77        nginx:1.13.0-alpine   "nginx -g 'daemon ..."   7 minutes ago       Up 7 minutes        80/tcp              nginx1.13.0
PS C:\Users\song> docker ps -ql
cdf8ba098d77
```  



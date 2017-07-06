## docker exec

命令参数

```
PS C:\Users\song> docker exec --help
Usage:  docker exec [OPTIONS] CONTAINER COMMAND [ARG...]
Run a command in a running container
Options:
  -d, --detach               Detached mode: run command in the background 分离模式:在后台运行命令
      --detach-keys string   Override the key sequence for detaching a container
  -e, --env list             Set environment variables 设置环境变量
      --help                 Print usage
  -i, --interactive          Keep STDIN open even if not attached 即使不附加，也要保持STDIN
      --privileged           Give extended privileges to the command
  -t, --tty                  Allocate a pseudo-TTY 分配一个虚拟TTY
  -u, --user string          Username or UID (format: <name|uid>[:<group|gid>])
```

### 应用实例

```
- 进入容器中操作
docker exec -it nginx1.13.0 /bin/sh 

```




## rmi rm

```
PS E:\home\docker\Dockerfile> docker rmi -h
Flag shorthand -h has been deprecated, please use --help

Usage:  docker rmi [OPTIONS] IMAGE [IMAGE...]

Remove one or more images

Options:
  -f, --force      Force removal of the image
      --help       Print usage
      --no-prune   Do not delete untagged parents
```




```
PS E:\home\docker\Dockerfile> docker rm -h
Flag shorthand -h has been deprecated, please use --help

Usage:  docker rm [OPTIONS] CONTAINER [CONTAINER...]

Remove one or more containers

Options:
  -f, --force     Force the removal of a running container (uses SIGKILL)
      --help      Print usage
  -l, --link      Remove the specified link
  -v, --volumes   Remove the volumes associated with the container
```

备注：
可以使用 docker rm $(docker ps -q -a) 一次性删除所有的容器，docker rmi $(docker images -q) 一次性删除所有的镜像。
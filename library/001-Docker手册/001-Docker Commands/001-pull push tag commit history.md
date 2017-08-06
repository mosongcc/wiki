## docker 版本管理操作

下载Docker镜像。

```
PS C:\Users\song> docker pull --help
Usage:  docker pull [OPTIONS] NAME[:TAG|@DIGEST]
Pull an image or a repository from a registry
Options:
  -a, --all-tags                Download all tagged images in the repository
      --disable-content-trust   Skip image verification (default true)
      --help                    Print usage
```


### docker commit
提交容器更新的内容到镜像文件。
```
PS E:\home\docker\Dockerfile> docker commit -h
Flag shorthand -h has been deprecated, please use --help

Usage:  docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]

Create a new image from a container's changes

Options:
  -a, --author string    Author (e.g., "John Hannibal Smith
                         <hannibal@a-team.com>")
  -c, --change list      Apply Dockerfile instruction to the created image
      --help             Print usage
  -m, --message string   Commit message
  -p, --pause            Pause container during commit (default true)
```

示例：
```
docker commit -m='类似git的提交备注信息' -a='Zengs' 79e53faada02  zingsono/nginx
```


### docker tag
对已存在镜像打标签。
```
PS E:\home\docker\Dockerfile> docker tag --help

Usage:  docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]

Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE

Options:
      --help   Print usage
```

示例：
```
docker tag zingsono/nginx zingsono/nginx:1.3.2
```

### docker push
推送镜像到镜像服务器。
```
PS E:\home\docker\Dockerfile> docker push --help

Usage:  docker push [OPTIONS] NAME[:TAG]

Push an image or a repository to a registry

Options:
      --disable-content-trust   Skip image signing (default true)
      --help                    Print usage
```




### docker pull
获取镜像服务器中的镜像资源。
```
PS E:\home\docker\Dockerfile> docker pull --help

Usage:  docker pull [OPTIONS] NAME[:TAG|@DIGEST]

Pull an image or a repository from a registry

Options:
  -a, --all-tags                Download all tagged images in the repository
      --disable-content-trust   Skip image verification (default true)
      --help                    Print usage
```

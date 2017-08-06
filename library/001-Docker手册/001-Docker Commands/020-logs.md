

The docker logs 显示所有的容器中terminal输出

The docker logs --follow command will continue streaming the new output from the container'sSTDOUT and STDERR.

Passing a negative number or a non-integer to --tail is invalid and the value is set to all in that case. This behavior may change in the future.

```
PS E:\home\docker\Dockerfile> docker logs --help

Usage:  docker logs [OPTIONS] CONTAINER

Fetch the logs of a container

Options:
      --details        Show extra details provided to logs
  -f, --follow         Follow log output
      --help           Print usage
      --since string   Show logs since timestamp (e.g.
                       2013-01-02T13:23:37) or relative (e.g. 42m for 42
                       minutes)
      --tail string    Number of lines to show from the end of the logs
                       (default "all")
  -t, --timestamps     Show timestamps
```


```
PS E:\home\docker\Dockerfile> docker start --help

Usage:  docker start [OPTIONS] CONTAINER [CONTAINER...]

Start one or more stopped containers

Options:
  -a, --attach                  Attach STDOUT/STDERR and forward signals
      --checkpoint string       Restore from this checkpoint
      --checkpoint-dir string   Use a custom checkpoint storage directory
      --detach-keys string      Override the key sequence for detaching a
                                container
      --help                    Print usage
  -i, --interactive             Attach container's STDIN
PS E:\home\docker\Dockerfile> docker stop --help

Usage:  docker stop [OPTIONS] CONTAINER [CONTAINER...]

Stop one or more running containers

Options:
      --help       Print usage
  -t, --time int   Seconds to wait for stop before killing it (default 10)
```
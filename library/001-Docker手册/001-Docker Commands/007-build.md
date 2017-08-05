
## docker build 命令使用

```
PS E:\home\docker\Dockerfile> docker build -h
Flag shorthand -h has been deprecated, please use --help

Usage:  docker build [OPTIONS] PATH | URL | -

Build an image from a Dockerfile

Options:
      --add-host list              Add a custom host-to-IP mapping (host:ip)
      --build-arg list             Set build-time variables
      --cache-from stringSlice     Images to consider as cache sources
      --cgroup-parent string       Optional parent cgroup for the container
      --compress                   Compress the build context using gzip
      --cpu-period int             Limit the CPU CFS (Completely Fair
                                   Scheduler) period
      --cpu-quota int              Limit the CPU CFS (Completely Fair
                                   Scheduler) quota
  -c, --cpu-shares int             CPU shares (relative weight)
      --cpuset-cpus string         CPUs in which to allow execution (0-3, 0,1)
      --cpuset-mems string         MEMs in which to allow execution (0-3, 0,1)
      --disable-content-trust      Skip image verification (default true)
  -f, --file string                Name of the Dockerfile (Default is
                                   'PATH/Dockerfile')
      --force-rm                   Always remove intermediate containers
      --help                       Print usage
      --iidfile string             Write the image ID to the file
      --isolation string           Container isolation technology
      --label list                 Set metadata for an image
  -m, --memory bytes               Memory limit
      --memory-swap bytes          Swap limit equal to memory plus swap:
                                   '-1' to enable unlimited swap
      --network string             Set the networking mode for the RUN
                                   instructions during build (default
                                   "default")
      --no-cache                   Do not use cache when building the image
      --pull                       Always attempt to pull a newer version
                                   of the image
  -q, --quiet                      Suppress the build output and print
                                   image ID on success
      --rm                         Remove intermediate containers after a
                                   successful build (default true)
      --security-opt stringSlice   Security options
      --shm-size bytes             Size of /dev/shm
      --squash                     Squash newly built layers into a
                                   single new layer
  -t, --tag list                   Name and optionally a tag in the
                                   'name:tag' format
      --target string              Set the target build stage to build.
      --ulimit ulimit              Ulimit options (default [])
PS E:\home\docker\Dockerfile> docker build

```
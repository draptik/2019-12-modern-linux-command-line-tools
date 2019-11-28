# Why?

People can try some of the tools which where illustrated in the session.

Without messing up there own system.

Using docker.

The docker container size: ~700MB (based on Ubuntu 19.10)

# Usage

```sh
# create the image
./build-container.sh

# start docker container
./run-container.sh
```

Within the docker container:

```sh
# start tmux session using byobu
# switch between `tabs` with `F3` and `F4`
./start-demos.sh
```

# TODOs

- inject sensible configs for the demo-tools

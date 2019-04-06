# Docker ROS GUI

This is docker images for ROS with Nvidia GPU and nvidia-docker2.
I support only `kinetic` and `indigo` because `melodic` is already supported by [osrf/ros](https://hub.docker.com/r/osrf/ros).


## Installation

If you want to use prebuild image,
```bash
$ docker pull arwtyxouymz/ros:<rosdistro>-gui
```

Or, you can build by yourself.
```bash
$ git clone https://github.com/arwtyxouymz/docker-ros-gui.git
$ cd docker-ros-gui
$ docker build ./<rosdistro> -t <your image name>
```
## Usage

### X server control

You need to change your X server control.
```
$ xhost +
```

### docker-compose
You can use my `docker-compose-example.yaml` for compose file.
```bash
$ cp docker-compose-example.yaml docker-compose.yaml
$ docker-compose up
```
In my example, `rviz` starts automatically.

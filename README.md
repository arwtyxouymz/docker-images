# Docker ROS

This is docker images for ROS and dev environment.


## Installation

You can use prebuild docker image from docker-hub,
```bash
$ docker pull arwtyxouymz/ros:<tags>
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

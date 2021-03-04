# ros-docker
Running ros using docker containers

## Requirements

- [Docker](https://www.docker.com/)
- [ROS Noectic](http://wiki.ros.org/noetic/Installation)
- [RVIZ](http://wiki.ros.org/rviz) (optional for visualization)

## Demos

### Slamtoolbox

Run a dockerized verison of the demo showed in this video: [https://www.youtube.com/watch?v=ftfMsA-UykQ](https://www.youtube.com/watch?v=ftfMsA-UykQ)

To start the demo run the following command:

```sh
docker-compose up -d
```

To clean up the containers run the following command:

```sh
docker-compose down
```

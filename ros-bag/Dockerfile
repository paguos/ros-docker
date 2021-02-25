FROM ros:noetic-ros-core

RUN export uid=${uid} gid=${gid} && \
    mkdir -p /home/ros && \
    echo "ros:x:${uid}:${gid}:ros,,,:/home/ros:/bin/bash" >> /etc/passwd && \
    echo "ros:x:${uid}:" >> /etc/group && \
    echo "ros ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/ros && \
    chmod 0440 /etc/sudoers.d/ros && \
    chown ${uid}:${gid} -R /home/ros

USER ros
ENV HOME /home/ros

RUN printf "source /opt/ros/noetic/setup.bash" >> /home/ros/.bashrc

WORKDIR ros-bag
COPY slam_toolbox_filtered.bag slam_toolbox_filtered.bag

CMD ["rosbag", "play", "slam_toolbox_filtered.bag"]
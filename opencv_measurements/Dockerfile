FROM ros:humble

RUN apt-get update
RUN apt-get install -y python3-pip
RUN pip install opencv-contrib-python==4.5.4.60 scipy
RUN apt install -y ros-humble-vision-opencv
WORKDIR /workspace/src
RUN git clone https://github.com/DominikUrbaniak/custom_interfaces.git
RUN git clone https://github.com/DominikUrbaniak/rc_module_measurements.git
WORKDIR /workspace
RUN mkdir -p data/docs
RUN . /opt/ros/humble/setup.sh && \
  colcon build

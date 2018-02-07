# RosDistro for BuildBot

This is for our private build farm.

udpate test for ansible checking3


## we should know how to install the ros packages
http://wiki.ros.org/wstool

```bash
apt-get install python-wstool build-essential
mkdir ~/ros_catkin_ws
cd ~/ros_catkin_ws
wstool init src
wstool merge -t src <rosinstall extension fils path>
wstool update -t src
rosdep install --from-paths src -i -y
source /opt/ros/indigo/setup.zsh
catkin_make
source devel/setup.zsh
rosrun py_trees py-trees-demo-sequence 
cd src/py_trees/tests
nosetests test_tree.py

```

# jetson-nano

$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
$ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
$ sudo apt update
$ sudo apt install ros-melodic-desktop
$ echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc 
$ source ~/.bashrc
Install and initialize rosdep. rosdep
$ sudo apt install python-rosdep python-rosinstall 
$ sudo rosdep init 
$ rosdep update
$ sudo apt-get install cmake python-catkin-pkg 
$ mkdir -p ~/catkin_ws/src 
$ cd ~/catkin_ws/
$ catkin_make
$ echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc 
$ source ~/.bashrc
$ cd ~/catkin_ws/src
$ git clone https://github.com/stereolabs/zed-ros-wrapper.git
$ cd ~/catkin_ws
$ rosdep install --from-paths src --ignore-src -r -y
$ catkin_make -DCMAKE_BUILD_TYPE=Release
$ roslaunch zed_display_rviz display_zed.launch
$ roslaunch zed_display_rviz display_zedm.launch 


# ros2-jazzy-install
Init of Jazzy on Ubuntu, check REAME file

```bash
sudo apt install software-properties-common
sudo add-apt-repository universe
sudo apt update && sudo apt install curl
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
sudo apt update
sudo apt upgrade
sudo apt install ros-jazzy-desktop
sudo apt install ros-jazzy-ros-base
sudo apt install ros-dev-tools

sudo apt install ros-jazzy-ros2-control ros-jazzy-ros2-controllers ros-jazzy-gazebo-ros2-control
sudo apt install ros-jazzy-gazebo-ros-pkgs
sudo apt install ros-jazzy-ros-core ros-jazzy-geometry2
sudo pip3 install setuptools
sudo apt-get install ros-jazzy-joint-state-publisher-gui ros-jazzy-xacro

sudo apt install ros-jazzy-navigation2
sudo apt install ros-jazzy-nav2-bringup
sudo apt install ros-jazzy-slam-toolbox

sudo apt install ros-jazzy-robot-localization
sudo apt install ros-jazzy-robot-state-publisher
sudo apt install ros-jazzy-rviz2

# sudo apt install ros-jazzy-teleop-twist-keyboard

sudo rosdep init
rosdep update
# src like ~/SnowCron/ros_projects/harsh
rosdep install --from-paths src --ignore-src --rosdistro jazzy -y

sudo apt install python3-colcon-common-extensions

# Note: changed API after this version
pip install opencv-contrib-python==4.6.0.66 
sudo apt install ros-jazzy-aruco
```

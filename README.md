# CPP Pkg in ROS 2
## Prerequisite
- [ROS 2 Humble](https://docs.ros.org/en/humble/Installation.html) and Setup
- Initialize a [Catkin Workspace](https://docs.ros.org/en/foxy/Tutorials/Beginner-Client-Libraries/Creating-A-Workspace/Creating-A-Workspace.html)
## Colcon Setup
1. Install [Colcon](https://colcon.readthedocs.io/en/released/) Command Extensions
```
sudo apt install python3-colcon-command-extensions
```
2. Setup Auto Completion Feature. Verify the colocon-argcomplete.bash file is there
```
cd /usr/share/colcon_argcomplete/hook
ls
```
3. Add the Auto Completion to bashrc. Start by opening it in your preferred editor. I use Vim.
```
vim ~/.bashrc  
```
4. Add the following line towards the end of your file. I added it after the ROS 2 source
```
source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash
```
## Build a Catkin Workspace in ROS 2
1. Begin by creating the structure directories. By convention the ROS 2 Workspace is the following
```
mkdir -p ros2_ws/src
```
2. Build your workspace
```
cd ros2_ws
colcon build
```
If you get an error. It is likely you have not installed (Colcon)[https://colcon.readthedocs.io/en/released/]
3. Add your workspace to your bashrc. Start by opening it in your preferred editor. I use Vim.
```
vim ~/.bashrc  
```
4. Add the following line towards the end of your file. I added it after the Colcon Argument Complete source.
```
source ~/ros2_ws/install/setup.bash
```
This source command assumes that you created your workspace from your home directory ~. You will have to modifiy it depending on where your catkin workspace was initialized
## Create a CPP Package
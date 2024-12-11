# inverted_pendulum_project

This is a quick simulation on Gazebo of the inverted pendulum cart created for the Controls Systems Laboratory course.

## Usage
```
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src
git clone https://github.com/Abanesjo/inverted_pendulum_project.git
cd ..
rosdep install --from-paths src --ignore-src -r -y
catkin build
```
You also need to install the gazebo co-simulator
```
cd src/inverted_pendulum_project/GazeboPlugin
mkdir build && cd build
cmake ..
make
```
Then, open the ```pendulum.slx``` file, which is similar to what is shown below.
![image](https://github.com/user-attachments/assets/0142eb72-ceaf-4ddd-94fc-55ed50f25edb)

Finally, in another terminal, run
```
export SVGA_VGPU10=0
source devel/setup.bash
roslaunch inverted_pendulum gazebo.launch
```
You should see the simulation launch in Gazebo
![image](https://github.com/user-attachments/assets/be7d649c-2c5f-46a3-bebd-b906afa20ce9)

Make sure you use a fixed step size of 0.01 for the simulation.



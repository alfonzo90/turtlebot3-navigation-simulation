# turtlebot3-navigation-simulation
A documentation of the steps I took to run the turtlebot3 navigation simulation

This is a continutaiton of the steps i documented in the slam simulation repository

I will be executing the steps documented at https://emanual.robotis.com/docs/en/platform/turtlebot3/nav_simulation/


## launching the simulations
I'm starting things off by launching the simulation world

```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

Then run the navigation node

```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```

### after launching both simulations
![VirtualBoxVM_yqPc7aAfFo](https://user-images.githubusercontent.com/25144777/124663204-7695b600-deb2-11eb-9228-0fcfbf136174.png)


## Pose estimation
I used the '2D Pose Estimate' functionality a couple of times to manually input the robot's starting position and orientation until what the LDS sensor picked up lined up with the map

### robot after manually inputting its location on the map
![VirtualBoxVM_d5kDhwT1Qt](https://user-images.githubusercontent.com/25144777/124663416-b8bef780-deb2-11eb-9e76-76244c987eb3.png)


I then ran the keyboard teleoperation node and controlled the robot for a bit, so it has a more precise understanding of its environment and the obstacles around it

```
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

### robot after moving it for a bit
![VirtualBoxVM_a58Y2xp8Md](https://user-images.githubusercontent.com/25144777/124663747-279c5080-deb3-11eb-95fa-bfa037977864.png)


## autonomous navigation

I will simply click on the '2D Nav Goal' decide the goal position and orientation and the robot will autonomously reach the goal state




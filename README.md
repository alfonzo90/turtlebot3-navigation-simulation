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


## Pose estimation
I used the '2D Pose Estimate' functionality a couple of times to manually input the robot's starting position and orientation until what the LDS sensor picked up lined up with the map

### robot after manually inputting its location on the map
![VirtualBoxVM_fpbzuCNWvh](https://user-images.githubusercontent.com/25144777/124659485-b017f280-dead-11eb-8fe5-a40b930928e0.png)

I then ran the keyboard teleoperation node and controlled the robot for a bit, so it has a more precise understanding of its environment and the obstacles around it

```
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

### robot after moving it for a bit
![VirtualBoxVM_Xo3CZyOc7I](https://user-images.githubusercontent.com/25144777/124660361-c70b1480-deae-11eb-88bb-6c4ee4c83c92.png)


## autonomous navigation

I will simply click on the '2D Nav Goal' decide the goal position and orientation and the robot will autonomously reach the goal state




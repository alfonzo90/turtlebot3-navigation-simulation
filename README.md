# turtlebot3-navigation-simulation
A documentation of the steps I took to run the turtlebot3 navigation simulation

This is a continutaiton of the steps i documented in the slam simulation repository

I will be executing the steps documented at https://emanual.robotis.com/docs/en/platform/turtlebot3/nav_simulation/

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

I used the '2D Pose Estimate' functionality a couple of times to manually input the robot's starting position and orientation

![VirtualBoxVM_fpbzuCNWvh](https://user-images.githubusercontent.com/25144777/124659485-b017f280-dead-11eb-8fe5-a40b930928e0.png)


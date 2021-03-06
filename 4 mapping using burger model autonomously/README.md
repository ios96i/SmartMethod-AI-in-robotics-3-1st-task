 ## 4.mapping using burger model autonomously 

![](https://emanual.robotis.com/assets/images/platform/turtlebot3/simulation/turtlebot3_world_bugger.png)

 open **terminal** ctrl+alt+T 
 
 * TurtleBot3 World
 
 ```
 $ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch 
```

the simulation will open

![](https://emanual.robotis.com/assets/images/platform/turtlebot3/simulation/turtlebot3_world_bugger.png)

[**turtle world and scan**](https://github.com/ios96i/SmartMethods-internship-AI-in-robotics-3/blob/master/4%20mapping%20using%20burger%20model%20autonomously/turtle%20world%20and%20scan.png)

then we have to open the **map** 

open new terminal

lunch **SLIM**
```
export TURTLEBOT3_MODEL=burger 
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```

![](https://emanual.robotis.com/assets/images/platform/turtlebot3/simulation/virtual_slam.png)

to make a first move you can do it manualy or autonomously 
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch #for manulay using keybord 
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch #atounomosly drive by it self
```

to save map 

`$ rosrun map_server map_saver -f ~/map`

the result [**here**](https://github.com/ios96i/SmartMethods-internship-AI-in-robotics-3/blob/master/4%20mapping%20using%20burger%20model%20autonomously/Result%20fullscan.png)

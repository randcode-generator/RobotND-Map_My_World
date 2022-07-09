# RobotND - Map My World

This is the fourth project for the Udacity [Robotics Software Engineer](https://www.udacity.com/course/robotics-software-engineer--nd209) course. The objective of this project is to map the office the robot is in. The map of the office is built by moving the robot manually throughout the office.


While the robot is moving, the image and location is saved into a database. We use ```rtabmap-databaseViewer``` to read the database.
![](images/image1.png 'image1')

## How to build
```
mkdir -p catkin_ws/src
cd catkin_ws
cp -r ../RobotND-Map_My_World/* src/
catkin_make
```

## How to run
Open a terminal and run the following
```
cd <path to catkin>/catkin_ws/
source devel/setup.bash
roslaunch my_robot world.launch
```

Open a new terminal and run the following
```
cd <path to catkin>/catkin_ws/
source devel/setup.bash
roslaunch my_robot teleop.launch
```

Open a new terminal and run the following
```
cd <path to catkin>/catkin_ws/
source devel/setup.bash
roslaunch my_robot mapping.launch
```

After exploration of the office is complete, view the database
```
rtabmap-databaseViewer <path to rtabmap.db>
```

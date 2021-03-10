# Office world simulation

Launch pedsim RVIZ simulation
```bash
$ roslaunch pedsim_swarm_simulation pedsim_office_populated.launch
```

Equip jackal with realsense camera and spawn robot. Run in the same terminal window
```bash
$ export JACKAL_URDF_EXTRAS=/home/robot/catkin_ws_swarm/src/cpr_gazebo/jackal_files/realsense.urdf.xacro
$ roslaunch cpr_office_gazebo office_world_with_plugin.launch
```

Turn on AMCL and map_server for navigation in the defined map
```bash
$ roslaunch jackal_navigation amcl_demo.launch map_file:=/home/robot/catkin_ws_swarm/src/cpr_gazebo/cpr_office_map/mymap.yaml
```

Launch top-view RVIZ for navigation
```bash
$ roslaunch jackal_viz view_robot.launch config:=localization
```

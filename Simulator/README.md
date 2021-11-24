# Simulator Topics
This file contains some interesting topics and their relative message type published by the simulator. There are some more topics published not reported here. To investigate all of them run the command 
```bash
rostopic list -v
```

or use the [rqt_graph](http://wiki.ros.org/rqt_graph) while the simulator is running.

### Published Topics
- /carla/ego_vehicle/vehicle_status [carla_msgs/CarlaEgoVehicleStatus](https://github.com/carla-simulator/ros-bridge/blob/0.9.6/carla_msgs/msg/CarlaEgoVehicleStatus.msg)
- /carla/ego_vehicle/vehicle_info [carla_msgs/CarlaEgoVehicleInfo](https://github.com/carla-simulator/ros-bridge/blob/0.9.6/carla_msgs/msg/CarlaEgoVehicleInfo.msg)
- /carla/markers [visualization_msgs/MarkerArray](http://docs.ros.org/en/noetic/api/visualization_msgs/html/msg/MarkerArray.html)
- /carla/markers/static [visualization_msgs/MarkerArray](http://docs.ros.org/en/noetic/api/visualization_msgs/html/msg/MarkerArray.html)
- /carla/ego_vehicle/rgb_front/camera_info [sensor_msgs/CameraInfo](http://docs.ros.org/en/melodic/api/sensor_msgs/html/msg/CameraInfo.html)
- /carla/ego_vehicle/rgb_front/image [sensor_msgs/Image](http://docs.ros.org/en/noetic/api/sensor_msgs/html/msg/Image.html)
- /carla/ego_vehicle/depth_front/camera_info [sensor_msgs/CameraInfo](http://docs.ros.org/en/melodic/api/sensor_msgs/html/msg/CameraInfo.html)
- /carla/ego_vehicle/depth_front/image [sensor_msgs/Image](http://docs.ros.org/en/noetic/api/sensor_msgs/html/msg/Image.html)
- /carla/ego_vehicle/rgb_view/camera_info [sensor_msgs/CameraInfo](http://docs.ros.org/en/melodic/api/sensor_msgs/html/msg/CameraInfo.html)
- /carla/ego_vehicle/rgb_view/image [sensor_msgs/Image](http://docs.ros.org/en/noetic/api/sensor_msgs/html/msg/Image.html)
- /carla/ego_vehicle/lidar [sensor_msgs/PointCloud2](https://docs.ros.org/en/api/sensor_msgs/html/msg/PointCloud2.html)
- /carla/ego_vehicle/gnss [sensor_msgs/NavSatFix](http://docs.ros.org/en/api/sensor_msgs/html/msg/NavSatFix.html)
- /carla/ego_vehicle/imu [sensor_msgs/Imu](http://docs.ros.org/en/api/sensor_msgs/html/msg/Imu.html)
- /carla/ego_vehicle/collision [carla_msgs/CarlaCollisionEvent](https://github.com/carla-simulator/ros-bridge/blob/0.9.6/carla_msgs/msg/CarlaCollisionEvent.msg)
- /carla/ego_vehicle/lane_invasion [carla_msgs/CarlaLaneInvasionEvent](https://github.com/carla-simulator/ros-bridge/blob/0.9.6/carla_msgs/msg/CarlaLaneInvasionEvent.msg)
- /carla/ego_vehicle/odometry [nav_msgs/Odometry](http://docs.ros.org/en/noetic/api/nav_msgs/html/msg/Odometry.html)
- /carla/ego_vehicle/speedometer [std_msgs/Float32](http://docs.ros.org/en/noetic/api/std_msgs/html/msg/Float32.html)

### Control the vehicle
When spawning the vehicle through the `spawn_vehicle.launch` file, the [carla_manual_control](https://carla.readthedocs.io/projects/ros-bridge/en/latest/carla_manual_control/) package from *carla-ros-bridge* is also run.
Therefore the vehicle can be controlled by publishing on the topic
```bash
/carla/ego_vehicle/vehicle_control_cmd
```
 the [CarlaEgoVehicleControl message](https://github.com/MPC-Berkeley/carla-ros-bridge/blob/master/carla_msgs/msg/CarlaEgoVehicleControl.msg) .
 This way of controlling the simulated vehicle is momentary and it should be replaced as soon as possible by a bridge that will read as input's topics the same topics that the real e-team vehicle understands. 
These topics depends on the final ROS deployment on the e-team vehicle and they will be available soon. So, for testing use the above reported topic, this page will be then updated once the bridge is ready.




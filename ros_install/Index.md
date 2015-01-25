---
layout: page
title: ros_install 
permalink: /ros_install/
---
#Errors and solution to the errors while installing ros

###pointcloud_to_laserscan package cannot link
Solution:
-remove the pointcloud_to_laserscan package from build_isolated folder
-According to [this](https://github.com/ros-perception/perception_pcl/issues/71) thread replace the perception_pcl package in 'workspace'/src with [this repo](https://github.com/ros-perception/perception_pcl)
-compile again, if replacement didn't work then remove the pointcloud_to_laserscan folder from src/ and build_isolated/ and compile again



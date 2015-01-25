---
layout: page
title: ros_install 
permalink: /ros_install/
---

Errors and solution to the errors while installing ros
---------------------

###pointcloud_to_laserscan package cannot link

* remove the pointcloud_to_laserscan package from build_isolated folder

* According to [this](https://github.com/ros-perception/perception_pcl/issues/71) thread replace the perception_pcl package in 'workspace'/src with [this repo](https://github.com/ros-perception/perception_pcl)

* compile again, if replacement didn't work then remove the pointcloud_to_laserscan folder from src/ and build_isolated/ and compile again

###Failed to process package 'pcl_ros'

* cd into build_isolated/pcl_ros/ and do "ccmake ../../src/perception_pcl/pcl_ros"

* change the GLEW_INCLUDE_DIR to /usr/local/Cellar/glew/1.11.0/include/GL (if using brew)

* change the GLEW_GLEW_LIBRARY to /usr/local/Cellar/glew/1.11.0/lib

###Failed to process package 'rviz' - Parse error at "BOOST_JOIN"

* check the post [here](http://answers.ros.org/question/56056/boost-error-building-catkin-on-os-x/)



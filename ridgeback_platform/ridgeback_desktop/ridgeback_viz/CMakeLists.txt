cmake_minimum_required(VERSION 2.8.3)
project(ridgeback_viz)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()

roslaunch_add_file_check(launch/view_model.launch)
roslaunch_add_file_check(launch/view_robot.launch)
roslaunch_add_file_check(launch/view_diagnostics.launch)

install(DIRECTORY launch rviz rqt
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

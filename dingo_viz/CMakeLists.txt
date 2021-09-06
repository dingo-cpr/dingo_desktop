################################################################################
# Set minimum required version of cmake, project name and compile options
################################################################################
cmake_minimum_required(VERSION 3.5)
project(dingo_viz)

################################################################################
# Find ament packages and libraries for ament and system dependencies
################################################################################
find_package(ament_cmake REQUIRED)

################################################################################
# Install
################################################################################
install(
	DIRECTORY launch rviz
  DESTINATION share/${PROJECT_NAME}
)

# if(CATKIN_ENABLE_TESTING)
#   find_package(roslaunch REQUIRED)
#   roslaunch_add_file_check(launch/view_model.launch)
#   roslaunch_add_file_check(launch/view_robot.launch)
# endif()

################################################################################
# Macro for ament package
################################################################################
ament_package()

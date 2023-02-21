cmake_minimum_required(VERSION 3.5)
project(pacmod_interface)

find_package(autoware_cmake REQUIRED)
autoware_package()

ament_auto_add_executable(pacmod_additional_debug_publisher
  src/pacmod_additional_debug_publisher/pacmod_additional_debug_publisher_node.cpp
  src/pacmod_additional_debug_publisher/pacmod_additional_debug_publisher_main.cpp
)

ament_auto_add_executable(pacmod_dynamic_parameter_changer
  src/pacmod_dynamic_parameter_changer/pacmod_dynamic_parameter_changer_node.cpp
  src/pacmod_dynamic_parameter_changer/pacmod_dynamic_parameter_changer_main.cpp
)

ament_auto_add_executable(pacmod_interface
  src/pacmod_interface/pacmod_interface.cpp
  src/pacmod_interface/pacmod_interface_node.cpp
)

ament_auto_add_executable(pacmod_diag_publisher
  src/pacmod_interface/pacmod_diag_publisher.cpp
  src/pacmod_interface/pacmod_diag_publisher_node.cpp
)

ament_auto_add_executable(pacmod_steer_test
  src/pacmod_steer_test/pacmod_steer_test.cpp
  src/pacmod_steer_test/pacmod_steer_test_node.cpp
)

ament_auto_package(
  INSTALL_TO_SHARE
  launch
  config
)

cmake_minimum_required(VERSION 2.8.3)
project(naivphys4rp_msgs)

## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp rospy std_msgs geometry_msgs genmsg actionlib_msgs)

## Declare ROS messages and services
add_message_files(DIRECTORY msg FILES OntologyDescription.msg)
add_action_files(DIRECTORY action FILES LoadOntology.action SubClass.action ObjectProperty.action DataProperty.action NewIndividual.action ListClass.action ListProperty.action QueryKnowledge.action CommonPose.action)
## add_service_files(FILES AddTwoInts.srv)

## Generate added messages and services
generate_messages(DEPENDENCIES std_msgs geometry_msgs actionlib_msgs)

## Declare a catkin package
catkin_package()

## Build talker and listener
## include_directories(include ${catkin_INCLUDE_DIRS})

## add_executable(talker src/talker.cpp)
## target_link_libraries(talker ${catkin_LIBRARIES})
## add_dependencies(talker beginner_tutorials_generate_messages_cpp)

## add_executable(listener src/listener.cpp)
## target_link_libraries(listener ${catkin_LIBRARIES})
## add_dependencies(listener beginner_tutorials_generate_messages_cpp)

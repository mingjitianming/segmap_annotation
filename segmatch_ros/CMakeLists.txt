cmake_minimum_required(VERSION 2.8.3)
project(segmatch_ros)

add_definitions(-std=c++11 -DBENCHMARK_ENABLE)

find_package(catkin_simple 0.1.0 REQUIRED)

#find_package(catkin_simple 0.1.0 REQUIRED COMPONENTS
#    roscpp
#    rospy
#    std_msgs
#    genmsg
#    tf
#    rosbag
#    visualization_msgs
#####################################
#    message_generation
#
 
catkin_simple(ALL_DEPS_REQUIRED)

cs_add_library(${PROJECT_NAME} 
    src/segmatch_worker.cpp
)
     
#find_package(Boost REQUIsRED COMPONENTS system thread)   #原本有， 但出问题了  故注释掉

#add_doxygen(NOT_AUTOMATIC)

cs_install()
cs_export()


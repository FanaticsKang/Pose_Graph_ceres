#
# The interface of pose graph by Ceres And G2O  
# Author: Kang Yifei
# Email: ccyclonel@126.com
#

cmake_minimum_required( VERSION 2.8 )
project( Pose_Graph )

set( CMAKE_BUILD_TYPE "Debug" )
set( CMAKE_CXX_FLAGS "-std=c++11 -O3" )

#ceres
find_package( Ceres REQUIRED )
include_directories( ${CERES_INCLUDE_DIRS} )

message(CERES_INCLUDE_DIRS: ${CERES_INCLUDE_DIRS})

#find_package(gflags REQUIRED)


	
add_executable(pose_graph_3d pose_graph_3d.cc)
target_link_libraries(pose_graph_3d ceres ${CERES_INCLUDE_DIRS})


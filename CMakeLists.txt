cmake_minimum_required(VERSION 2.4.6)
include($ENV{ROS_ROOT}/core/rosbuild/rosbuild.cmake)

# Set the build type.  Options are:
#  Coverage       : w/ debug symbols, w/o optimization, w/ code-coverage
#  Debug          : w/ debug symbols, w/o optimization
#  Release        : w/o debug symbols, w/ optimization
#  RelWithDebInfo : w/ debug symbols, w/ optimization
#  MinSizeRel     : w/o debug symbols, w/ optimization, stripped binaries
#set(ROS_BUILD_TYPE RelWithDebInfo)

rosbuild_init()

#set the default path for built executables to the "bin" directory
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#set the default path for built libraries to the "lib" directory
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

#uncomment if you have defined messages
#rosbuild_genmsg()
#uncomment if you have defined services
#rosbuild_gensrv()

#common commands for building c++ executables and libraries
#rosbuild_add_library(${PROJECT_NAME} src/example.cpp)
#target_link_libraries(${PROJECT_NAME} another_library)
#rosbuild_add_boost_directories()
#rosbuild_link_boost(${PROJECT_NAME} thread)

#rosbuild_add_executable(vereshchagintest-2dof-motion src/vereshchagintest-2-dof-motion-matlab.cpp)
#rosbuild_add_executable(vereshchagintest-4dof-motion src/vereshchagintest-4-dof-motion-matlab.cpp)
rosbuild_add_executable(vereshchagintest-4dof-motion src/vereshchagintest-4-dof-motion-with-posture-matlab.cpp)
rosbuild_add_executable(vereshchagintest-youbot-motion src/vereshchagintest-youbot-motion-matlab.cpp)
rosbuild_add_executable(vereshchagintest-lwr-motion src/vereshchagintest-lwr-motion-matlab.cpp)
rosbuild_add_executable(vereshchagintest-baxter-motion src/vereshchagintest-baxter-motion-matlab.cpp)

#target_link_libraries(example ${PROJECT_NAME})

cmake_minimum_required(VERSION 3.0)

project(Todo)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g -Wall")

#是否可调试
set(CMAKE_BUILD_TYPE Debug)

 #相关库文件的目录
LINK_DIRECTORIES(                                 
/usr/local/lib
)

 #设置变量，表示所有的源文件
SET(SOURCE_FILES                                 
main.cpp
src/tool.cpp
src/hello/hello.cpp
)

#增加头文件目录
include_directories(
/usr/local/include
${CMAKE_SOURCE_DIR}/include
${CMAKE_SOURCE_DIR}/include/hello
)


add_executable(Todo_app ${SOURCE_FILES})
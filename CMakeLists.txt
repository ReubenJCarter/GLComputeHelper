cmake_minimum_required(VERSION 2.6)
project(GLComputeHelper)
set(PROJECT_BRIEF "GlComputeHelper")
set(CMAKE_BUILD_TYPE RELEASE)
set(GCC_COMPILE_FLAGS "-std=c++11 -Wall -O3 -g")
set(GCC_LINK_FLAGS "")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${GCC_COMPILE_FLAGS}")
set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} ${GCC_LINK_FLAGS}")

#GLFW

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/vendor/glfw-3.2.1/include)
link_directories(${CMAKE_CURRENT_SOURCE_DIR}/vendor/glfw-3.2.1/build/src/Release)

#GLEW

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/vendor/glew-2.0.0/include)
link_directories(${CMAKE_CURRENT_SOURCE_DIR}/vendor/glew-2.0.0/lib/Release/x64)
add_definitions(-DGLEW_STATIC)


include_directories(${CMAKE_CURRENT_SOURCE_DIR}/src)

add_subdirectory(src)
add_subdirectory(test)
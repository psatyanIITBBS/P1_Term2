project(EclipseExtendedKF)

cmake_minimum_required (VERSION 3.5)

add_definitions(-std=c++11)

set(CXX_FLAGS "-Wall")
set(CMAKE_CXX_FLAGS "${CXX_FLAGS}")

set(sources ./main.cpp ./tools.cpp ./FusionEKF.cpp ./kalman_filter.cpp ./tools.h ./FusionEKF.h ./kalman_filter.h)

add_executable(ExtendedKF ${sources})

target_link_libraries(ExtendedKF z ssl uv uWS)

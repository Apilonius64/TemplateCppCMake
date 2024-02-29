cmake_minimum_required(VERSION 3.0)
project(myproject)

file(GLOB_RECURSE sources src/main/*.cpp src/main/*.h)
file(GLOB_RECURSE data res/*)

add_executable(myproject ${sources})
target_include_directories(myproject PUBLIC src/)

file(COPY ${data} DESTINATION res)
cmake_minimum_required(VERSION 3.10)
project(app)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
find_package(SDL3 REQUIRED)

include_directories(./include/)
add_executable(${PROJECT_NAME} main.cpp
  src/Player.cpp
)

target_link_libraries(${PROJECT_NAME} PRIVATE SDL3::SDL3)


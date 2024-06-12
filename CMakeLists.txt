cmake_minimum_required(VERSION 3.10)
project(Gunship)

set(CMAKE_CXX_STANDARD 17)

include_directories(include)


# Find SDL2
find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIRS})

add_executable(Gunship src/main.cpp)


# Link SDL2
target_link_libraries(Gunship ${SDL2_LIBRARIES})

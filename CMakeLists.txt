cmake_minimum_required(VERSION 3.10)
project(app)

add_subdirectory(MinGL2_IUT_AIX)

set(CMAKE_CXX_STANDARD 17)

add_executable(app src/main.cpp)
target_include_directories(app PUBLIC include)

target_link_libraries(app mingl)

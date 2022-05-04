cmake_minimum_required(VERSION 3.22)
project(MinGL)

set(CMAKE_CXX_STANDARD 23)

file(GLOB_RECURSE LIB_HEADERS libs/*)
file(GLOB_RECURSE SRC src/*)
add_executable(MinGL ${LIB_HEADERS} ${SRC})
target_include_directories(MinGL PUBLIC src)

target_include_directories(MinGL PUBLIC libs)
target_link_directories(MinGL PUBLIC .)

target_link_libraries(MinGL GL)
target_link_libraries(MinGL GLU)
target_link_libraries(MinGL glut)
target_link_libraries(MinGL mingl)

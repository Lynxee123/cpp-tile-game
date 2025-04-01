cmake_minimum_required(VERSION 3.10.0)
project(tilegame VERSION 0.1.0 LANGUAGES C CXX)

add_executable(tilegame src/main.cpp)

set(CMAKE_CXX_STANDARD 20)
set(SFML_STATIC_LIBRARIES TRUE)
include_directories(lib/sfml/include)
add_subdirectory(lib/sfml/)
target_link_libraries(tilegame PRIVATE SFML::Graphics)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
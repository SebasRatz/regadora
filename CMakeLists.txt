cmake_minimum_required(VERSION 3.9)
project(regadora)

set(CMAKE_CXX_STANDARD 11)
# set the path to the library folde
find_library(RASPICO_LIBRARY raspberry_controls)

include_directories(regadora ../raspberry_controls/include)

# link the libraries to the executable
add_executable(regadora main.cpp)
target_link_libraries (regadora ${RASPICO_LIBRARY})

cmake_minimum_required(VERSION 3.11.3)

set(CMAKE_CXX_STANDARD 17)

project(HelloWorld)

find_package(wxWidgets REQUIRED COMPONENTS core base)
include(${wxWidgets_USE_FILE})

file(GLOB project_SRCS src/*.cpp)

add_executable(HelloWorld ${project_SRCS})
target_link_libraries(HelloWorld ${wxWidgets_LIBRARIES})
target_include_directories(HelloWorld PRIVATE ${wxWidgets_INCLUDE_DIRS})

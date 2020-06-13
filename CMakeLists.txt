cmake_minimum_required(VERSION 3.16)
project(obsidian)

set(CMAKE_CXX_STANDARD 20)
find_package(Vulkan REQUIRED)
find_package(glfw3 REQUIRED)
find_package(glm REQUIRED)

add_executable(obsidian main.cpp)
target_include_directories(obsidian PUBLIC ${Vulcan_INCLUDE_DIRS})
target_link_libraries(obsidian glfw glm Vulkan::Vulkan)

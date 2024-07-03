cmake_minimum_required(VERSION 3.10)
project(Vulkan)

set(CMAKE_CXX_STANDARD 17)
find_package(Vulkan REQUIRED)

add_subdirectory(submodules/glfw)
SET(GLM_TEST_ENABLE OFF CACHE BOOL "GLM Build unit tests")
add_subdirectory(submodules/glm EXCLUDE_FROM_ALL)

add_executable(${PROJECT_NAME} src/Application.cpp)

target_link_libraries(${PROJECT_NAME} glfw ${GLFW_LIBRARIES} Vulkan::Vulkan glm::glm)
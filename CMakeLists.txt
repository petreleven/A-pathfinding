cmake_minimum_required(VERSION 3.5)
project(game)

add_subdirectory(raylib)
add_subdirectory(imgui)
add_executable(game game.cpp)
target_link_libraries(game PUBLIC raylib imgui imgui_impl_glfw rlImGui)
target_include_directories(game PUBLIC 
              "${PROJECT_BINARY_DIR}"
               "${PROJECT_SOURCE_DIR}/raylib"
              "${PROJECT_SOURCE_DIR}/imgui")

# specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

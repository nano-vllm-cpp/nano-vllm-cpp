cmake_minimum_required(VERSION 3.25)
project(nano_vllm_cpp VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(nano_vllm_cpp src/main.cpp)
target_include_directories(nano_vllm_cpp PRIVATE ${CMAKE_SOURCE_DIR}/include)

find_package(spdlog CONFIG REQUIRED)
target_link_libraries(nano_vllm_cpp PRIVATE spdlog::spdlog_header_only)
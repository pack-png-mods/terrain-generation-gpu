cmake_minimum_required(VERSION 3.16)
project(TerrainGenGPU LANGUAGES CUDA)

set(CMAKE_CUDA_STANDARD 14)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Ofast -Wall -pedantic -ggdb3 ")
add_executable(TerrainGenGPU main.cu)

set_target_properties(
        TerrainGenGPU
        PROPERTIES
        CUDA_SEPARABLE_COMPILATION ON)
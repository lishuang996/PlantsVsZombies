cmake_minimum_required(VERSION 4.0)
project(PlantsVsZombies)

# 采用C++20标准
set(CMAKE_CXX_STANDARD 20)

# 定义SDL2的根目录、include目录和库目录
set (SDL_PATH "${CMAKE_SOURCE_DIR}/lib/SDL2-2.32.10")
set (SDL_INCLUDE_PATH ${SDL_PATH}//include)
set (SDL_LIB_PATH ${SDL_PATH}//lib//x64)

# 定义SDL2的库
set (SDL_LIBS ${SDL_LIB_PATH}/SDL2.lib ${SDL_LIB_PATH}/SDL2main.lib ${SDL_LIB_PATH}/SDL2.dll)

# 添加include目录
include_directories(${SDL_INCLUDE_PATH})

# 添加库目录
link_directories(${SDL_LIB_PATH})

add_executable(PlantsVsZombies main.cpp)

# 对所需的库进行链接
target_link_libraries(PlantsVsZombies ${SDL_LIBS})

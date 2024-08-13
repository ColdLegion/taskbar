cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDART 17)
set(CMAKE_CXX_STANDART_REQUIRED ON)
set(CMAKE_C_COMPILER /usr/bin/x86_64-w64-mingw32-gcc)
set(CMAKE_CXX_COMPILER /usr/bin/x86_64-w64-mingw32-g++)
set(CMAKE_CXX_FLAGS "-static")

project(taskbar)

file(GLOB_RECURSE SRC_FILES src/*.cpp) # Recursively grab all .cpp files
add_executable(taskbar ${SRC_FILES})
target_include_directories(taskbar PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src) # Include header files

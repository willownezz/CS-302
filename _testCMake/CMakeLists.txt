#cmake_minimum_required(VERSION 3.0)
cmake_minimum_required(VERSION 3.5)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14")



#Project Name
project(_testCMake2)

add_executable(
    helloWorldCMake
    main.cpp
    functions.h
    functions1.cpp
    functions2.cpp
    )



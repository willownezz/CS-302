cmake_minimum_required(VERSION 3.0)
#cmake_minimum_required(VERSION "3.5.1")

#add_compile_options()
#target_compile_features()



set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14")

#Project Name
project(_testCMake)

add_executable(
    #helloWorldCMake
    "${PROJECT_NAME}"
    "main.cpp"
    )



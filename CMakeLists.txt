cmake_minimum_required(VERSION 3.15)
project(Test)


set(CMAKE_CXX_STANDARD 11)


link_directories("/opt/intel/sgxsdk/lib64/")


add_executable(Test main.cpp)

target_include_directories(Test PRIVATE /opt/intel/sgxsdk/include/)

target_link_libraries(Test sgx_capable)
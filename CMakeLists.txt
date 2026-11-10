cmake_minimum_required(VERSION 3.16)
project(CppStudy LANGUAGES CXX)

add_executable(main src/main.cpp src/copy.cpp)

target_compile_features(main PRIVATE cxx_std_17)
target_include_directories(main PRIVATE include)
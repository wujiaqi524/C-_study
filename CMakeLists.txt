cmake_minimum_required(VERSION 3.16)
project(CppStudy LANGUAGES CXX)

#用copy.cpp构建静态库
add_library(greeting STATIC src/copy.cpp)
target_compile_features(greeting PRIVATE cxx_std_17)
target_include_directories(greeting PUBLIC include)

#构建程序，并链接 greeting 库
add_executable(main src/main)
target_compile_features(main PRIVATE cxx_std_17)
target_link_libraries(main PRIVATE greeting)

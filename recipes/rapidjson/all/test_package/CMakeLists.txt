cmake_minimum_required(VERSION 3.15)
project(test_package)

find_package(RapidJSON CONFIG REQUIRED)

add_executable(${PROJECT_NAME} test_package.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE rapidjson)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_11)

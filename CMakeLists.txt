cmake_minimum_required(VERSION 3.15)

project(fibo CXX)

find_package(fmt REQUIRED)
find_package(range-v3 REQUIRED)
find_package(cxxopts REQUIRED)

add_executable(fibo src/main.cxx)
target_compile_features(fibo PRIVATE cxx_std_17)

target_link_libraries(fibo
  PRIVATE
    fmt::fmt
    range-v3::range-v3
    cxxopts::cxxopts)

cmake_minimum_required(VERSION 3.10)
project(furgbol)

include_directories("include"
  "lib/RxCpp/Rx/v2/src")

add_library(furgbol_io SHARED
  "src/io/multicast_receiver.cc")

add_executable(testing "src/main.cpp")
target_link_libraries(testing furgbol_io)

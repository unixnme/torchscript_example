cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(custom_ops)

set(CMAKE_PREFIX_PATH /Users/ykang/Repos/ctcdecode_private/third_party/libtorch)
find_package(Torch REQUIRED)

add_executable(example-app main.cc)
target_link_libraries(example-app "${TORCH_LIBRARIES}")
set_property(TARGET example-app PROPERTY CXX_STANDARD 11)

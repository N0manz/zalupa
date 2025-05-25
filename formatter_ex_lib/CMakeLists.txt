cmake_minimum_required(VERSION 3.10)
project(formatter_ex_lib)

include_directories(${PROJECT_SOURCE_DIR}/../formatter_lib)

add_library(formatter_ex STATIC
    formatter_ex.cpp
)

target_link_libraries(formatter_ex PRIVATE formatter)

target_include_directories(formatter_ex PUBLIC
    ${PROJECT_SOURCE_DIR}
)

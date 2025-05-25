cmake_minimum_required(VERSION 3.10)
project(formatter_lib)

add_library(formatter STATIC
    formatter.cpp
)

target_include_directories(formatter PUBLIC
    ${PROJECT_SOURCE_DIR}
)

install(TARGETS formatter ARCHIVE DESTINATION lib)
install(DIRECTORY ${PROJECT_SOURCE_DIR}/ DESTINATION include/formatter)

# solver_lib/CMakeLists.txt

cmake_minimum_required(VERSION 3.10)
project(solver_lib)

# Создаем статическую библиотеку из solver.cpp
add_library(solver STATIC
    solver.cpp
)

# Указываем, где искать заголовочные файлы
target_include_directories(solver PUBLIC ${PROJECT_SOURCE_DIR})

# Опционально: установка
install(TARGETS solver ARCHIVE DESTINATION lib)
install(DIRECTORY ${PROJECT_SOURCE_DIR}/ DESTINATION include/solver)

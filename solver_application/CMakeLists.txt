# hello_world_application/CMakeLists.txt

cmake_minimum_required(VERSION 3.10)
project(solver_app)

# Указываем где искать заголовочные файлы
include_directories(
    ${PROJECT_SOURCE_DIR}/../formatter_ex_lib
    ${PROJECT_SOURCE_DIR}/../formatter_lib
    ${PROJECT_SOURCE_DIR}/../solver_lib
)

# Указываем где искать .a файлы
link_directories(
    ${PROJECT_SOURCE_DIR}/../formatter_ex_lib/build
    ${PROJECT_SOURCE_DIR}/../formatter_lib/build
    ${PROJECT_SOURCE_DIR}/../solver_lib/build
)

# Собираем исполняемый файл
add_executable(solver equation.cpp)

# Линкуемся с библиотеками по имени
target_link_libraries(solver PRIVATE
    formatter_ex
    formatter
    solver_lib
)

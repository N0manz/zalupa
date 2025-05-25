# hello_world_application/CMakeLists.txt

cmake_minimum_required(VERSION 3.10)
project(hello_world_application)

# Подключаем библиотеки
add_subdirectory(../formatter_lib formatter_lib_build)
add_subdirectory(../formatter_ex_lib formatter_ex_lib_build)

# Добавляем наше приложение
add_executable(hello_world hello_world.cpp)

# Линкуемся с библиотеками по имени
target_link_libraries(hello_world PRIVATE
    formatter_ex
    formatter
)

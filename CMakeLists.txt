cmake_minimum_required(VERSION 3.15)
project(SfmlGame VERSION 1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Поиск SFML
find_package(SFML 2.5 COMPONENTS graphics window system audio network REQUIRED)

# Создание исполняемого файла
add_executable(SfmlGame "sfml-game/main.cpp")

# Подключение заголовочных файлов и библиотек SFML
target_link_libraries(SfmlGame PRIVATE sfml-graphics sfml-window sfml-system)

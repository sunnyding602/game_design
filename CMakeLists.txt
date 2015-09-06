cmake_minimum_required (VERSION 2.6)
project (Tutorial)

# The version number.
set (Tutorial_VERSION_MAJOR 1)
set (Tutorial_VERSION_MINOR 0)
set(CMAKE_C_FLAGS "-Wall -g")


include_directories ("${PROJECT_SOURCE_DIR}/src")
add_subdirectory (src)
set (EXTRA_LIBS ${EXTRA_LIBS} src)

# add the executable
add_executable (Tutorial game.m.cpp)
target_link_libraries (Tutorial  ${EXTRA_LIBS})

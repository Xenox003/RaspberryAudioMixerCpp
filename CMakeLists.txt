cmake_minimum_required(VERSION 3.0.0)

get_filename_component(ProjectId ${CMAKE_CURRENT_LIST_DIR} NAME)
string(REPLACE " " "_" ProjectId ${ProjectId})

project(RaspberryAudioMixer VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(RaspberryAudioMixer main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

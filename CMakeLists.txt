cmake_minimum_required(VERSION 3.18)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

project(
    C-Certificate
    VERSION 0.1
    DESCRIPTION "CLP Certification"
    LANGUAGES C
    )

set_property(
    TARGET ${PROJECT}
    PROPERTY C_STANDARD 11
)

add_library(
    ${PROJECT_NAME}
    src/C1/src/c1-1.c
)

target_include_directories(
    ${PROJECT_NAME}
    PUBLIC
    include
    include/lab1-1
)

add_executable(
    "lab1-1"
    src/C1/src/c1-1.c
)
add_executable(
    "lab1-2"
    src/C1/src/c1-2.c
)
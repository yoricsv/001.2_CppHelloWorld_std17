cmake_minimum_required(VERSION 3.20)

    set( PROJECT_NAME
            HelloWorld
    )

    set( PROJECT_PROPERTIES
            CMAKE_BUILD_TYPE            Debug
            CMAKE_CXX_FLAGS             -O3
            CMAKE_CXX_FLAGS             -Wall
            CMAKE_CXX_STANDARD          17
            CMAKE_CXX_STANDARD_REQUIRED ON
            RUNTIME_OUTPUT_DIRECTORY    ${CMAKE_SOURCE_DIR}/out
    )

project( ${PROJECT_NAME}
            LANGUAGES
            CXX
)
    set( PROJECT_SOURCE_DIR
            ${PROJECT_NAME}/src
    )
    set( SOURCES
            main.cpp
    )

include_directories(${PROJECT_SOURCE_DIR})

add_executable(
        ${PROJECT_NAME}
             ${PROJECT_SOURCE_DIR}/${SOURCES}
)

set_target_properties(
        ${PROJECT_NAME}
    PROPERTIES
        ${PROJECT_PROPERTIES}
)
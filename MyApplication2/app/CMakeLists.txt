cmake_minimum_required(VERSION 3.4.1)

#SET (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O0 -g -fsanitize=address -fno-omit-frame-pointer")
#SET (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -O0 -g -fsanitize=address -fno-omit-frame-pointer")
#SET (CMAKE_SHARED_LINKER_FLAGS "${CMAKE_SHARED_LINKER_FLAGS} -fsanitize=address")

set(CMAKE_VERBOSE_MAKEFILE on)

# gif
set(SOURCES)
file(GLOB_RECURSE SOURCES src/main/cpp/gif/*.c)

add_library(pl_droidsonroids_gif SHARED ${SOURCES})

set(LIBS)
list(APPEND LIBS
        jnigraphics
        android
        GLESv2
        log
        )

target_link_libraries(pl_droidsonroids_gif ${LIBS})

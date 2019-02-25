cmake_minimum_required(VERSION 2.7)
project(Lua)

file(GLOB Lua_SOURCES src/*.c)

add_library(Lua ${Lua_SOURCES})

if(UNIX)
    target_link_libraries(Lua m)
endif(UNIX)

target_include_directories(Lua INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/src)

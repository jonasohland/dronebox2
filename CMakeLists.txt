cmake_minimum_required (VERSION 3.10)

project (dronebox2 VERSION 0.0.1 LANGUAGES CXX)

add_library(dronebox2 STATIC 
            ${CMAKE_CURRENT_LIST_DIR}/src/dronebox.cc)

target_include_directories(dronebox2 PUBLIC ${CMAKE_CURRENT_LIST_DIR}/include)
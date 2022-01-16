cmake_minimum_required (VERSION 3.13)

project (dronebox2 VERSION 0.0.1 LANGUAGES CXX)

set (CMAKE_POLICY_DEFAULT_CMP0077 NEW)
set (LIBSAMPLERATE_EXAMPLES OFF)
set (LIBSAMPLERATE_INSTALL OFF)
set (BUILD_TESTING OFF)
set (BUILD_SHARED_LIBS OFF)

add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/deps/libsamplerate)

add_library (dronebox2 STATIC 
            ${CMAKE_CURRENT_LIST_DIR}/src/dronebox.cc)

target_include_directories (dronebox2 PUBLIC ${CMAKE_CURRENT_LIST_DIR}/include)

target_link_libraries (dronebox2 PRIVATE SampleRate::samplerate)
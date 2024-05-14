cmake_minimum_required(VERSION 2.8) 
PROJECT (sandboxCV)
find_package(OpenCV REQUIRED )
set( NAME_SRC
    
    "src/histogram.cpp"
)

set( NAME_HEADERS
    
    "include/histogram.hpp"
)

INCLUDE_DIRECTORIES( ${CMAKE_CURRENT_SOURCE_DIR}/include )
link_directories( ${CMAKE_BINARY_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)
add_executable( sandboxCV ${NAME_SRC} ${NAME_HEADERS} )

target_link_libraries( sandboxCV ${OpenCV_LIBS} )
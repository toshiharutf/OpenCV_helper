cmake_minimum_required(VERSION 2.8) 
PROJECT (name)
find_package(OpenCV REQUIRED )
set( NAME_SRC
    src/main.cpp    
)

#set( NAME_HEADERS       
#     include/header.h
#)

INCLUDE_DIRECTORIES( ${CMAKE_CURRENT_SOURCE_DIR}/include )
#link_directories( ${CMAKE_BINARY_DIR}/bin)
link_directories( ${CMAKE_CURRENT_SOURCE_DIR}/bin)
#set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_CURRENT_SOURCE_DIR}/bin)
add_executable( main ${NAME_SRC} ${NAME_HEADERS} )

target_link_libraries( main ${OpenCV_LIBS} )

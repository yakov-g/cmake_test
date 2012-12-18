cmake_minimum_required(VERSION 2.8)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")

message("Prefix path: " "${CMAKE_PREFIX_PATH}")
find_package(Elementary REQUIRED)
find_package(Evas REQUIRED)
message("module path: " "${CMAKE_MODULE_PATH}")
message("elm found: " "${ELEMENTARY_FOUND}")
message("elm dirs: ""${ELEMENTARY_INCLUDE_DIRS}")
message("elm libs: ""${ELEMENTARY_LIBRARIES}")
message("elm defs: ""${ELEMENTARY_DEFINITIONS}")

#   message(SEND_ERROR "Failed to find Elementary")
if(NOT ELEMENTARY_FOUND)
   message(STATUS "Failed to find Elementary")
   return()
else()
   message(STATUS "Elementary Found")
endif()



add_subdirectory(src_main)
add_subdirectory(src)

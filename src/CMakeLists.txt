cmake_minimum_required(VERSION 2.8)

link_directories(${PC_LIBELEMENTARY_LIBRARY_DIRS})
add_executable(button button_example_01.c)

message(STATUS "pc_elem: " ${PC_LIBELEMENTARY_LIBRARIES})
message(STATUS "pc_elem: " ${PC_LIBELEMENTARY_LIBRARY_DIRS})
message(STATUS "incl dir: " ${PC_LIBELEMENTARY_INCLUDEDIR})
message(STATUS "incl_dirs: " ${PC_LIBELEMENTARY_INCLUDE_DIRS})
message(STATUS "rom_elem: " ${ELEMENTARY_LIBRARIES})

include_directories(${ELEMENTARY_INCLUDE_DIRS})
#target_link_libraries(button ${ELEMENTARY_LIBRARIES} ${EVAS_LIBRARIES})
target_link_libraries(button ${PC_LIBELEMENTARY_LIBRARIES} eo)

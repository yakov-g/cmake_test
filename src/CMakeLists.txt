cmake_minimum_required(VERSION 2.8)

add_executable(button button_example_01.c)

include_directories(${ELEMENTARY_INCLUDE_DIRS})
target_link_libraries(button ${ELEMENTARY_LIBRARIES} ${EVAS_LIBRARIES})

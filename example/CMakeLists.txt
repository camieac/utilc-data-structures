# Compile the example executable
add_executable(utilc-data-structures-example utilc-data-structures-example.c)
include_directories(../include/)
target_link_libraries(utilc-data-structures-example utilc-data-structures)

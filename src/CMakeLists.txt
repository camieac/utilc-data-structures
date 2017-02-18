# Bring in the headers and sources
include_directories(../include)
file(GLOB SOURCES "*.c")

# Generate the shared library from the sources
add_library(utilc-data-structures SHARED ${SOURCES})

# Compile with real-time, pthread, math libraries
target_link_libraries(utilc-data-structures rt pthread m subunit)

# Install system-wide
install(TARGETS utilc-data-structures DESTINATION /usr/lib)

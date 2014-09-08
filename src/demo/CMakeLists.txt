
set(DEMO_SOURCES main.cpp)
include_directories(.)
include_directories(../lib)
source_group(demo FILES ${DEMO_SOURCES})

add_executable(meanshift_demo ${DEMO_SOURCES})
target_link_libraries(meanshift_demo ${OpenCV_LIBS}
                                     meanshift)

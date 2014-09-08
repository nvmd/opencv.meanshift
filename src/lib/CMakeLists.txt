
set(LIBRARY_SOURCES MeanShift.cpp MeanShift.h)
include_directories(.)
source_group(lib FILES ${LIBRARY_SOURCES})

add_library(meanshift ${LIBRARY_SOURCES})

include_directories(${CMAKE_SOURCE_DIR}/ccutil)
include_directories(${CMAKE_SOURCE_DIR}/ccstruct)
include_directories(${CMAKE_SOURCE_DIR}/ccmain)

########### next target ###############

SET(tesseract_opencl_STAT_SRCS
   openclwrapper.cpp
)

add_library(tesseract_opencl_static STATIC ${tesseract_opencl_STAT_SRCS})
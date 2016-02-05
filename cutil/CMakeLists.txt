include_directories(${CMAKE_SOURCE_DIR}/ccutil)
include_directories(${CMAKE_SOURCE_DIR}/viewer)

########### next target ###############

SET(tesseract_cutil_STAT_SRCS
   bitvec.cpp
   callcpp.cpp
   cutil.cpp
   cutil_class.cpp
   danerror.cpp
   efio.cpp
   emalloc.cpp
   freelist.cpp
   listio.cpp
   oldlist.cpp
   structures.cpp
)

add_library(tesseract_cutil_static STATIC ${tesseract_cutil_STAT_SRCS})
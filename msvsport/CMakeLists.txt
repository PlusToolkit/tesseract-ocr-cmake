########### next target ###############

SET(tesseract_msvsport_STAT_SRCS
   gettimeofday.cpp
)

add_library(tesseract_msvsport_static STATIC ${tesseract_msvsport_STAT_SRCS})
include_directories(${CMAKE_SOURCE_DIR}/ccutil)

########### next target ###############

SET(tesseract_viewer_STAT_SRCS
   scrollview.cpp
   svmnode.cpp
   svutil.cpp
   svpaint.cpp
)

add_library(tesseract_viewer_static STATIC ${tesseract_viewer_STAT_SRCS})
include_directories(${CMAKE_SOURCE_DIR}/cutil)
include_directories(${CMAKE_SOURCE_DIR}/ccutil)
include_directories(${CMAKE_SOURCE_DIR}/ccstruct)
include_directories(${CMAKE_SOURCE_DIR}/viewer)
include_directories(${CMAKE_SOURCE_DIR}/opencl)

########### next target ###############

SET(tesseract_textord_STAT_SRCS
   alignedblob.cpp
   baselinedetect.cpp
   bbgrid.cpp
   blkocc.cpp
   blobgrid.cpp
   ccnontextdetect.cpp
   cjkpitch.cpp
   colfind.cpp
   colpartition.cpp
   colpartitionset.cpp
   colpartitiongrid.cpp
   devanagari_processing.cpp
   drawedg.cpp
   drawtord.cpp
   edgblob.cpp
   edgloop.cpp
   equationdetectbase.cpp
   fpchop.cpp
   gap_map.cpp
   imagefind.cpp
   linefind.cpp
   makerow.cpp
   oldbasel.cpp
   pithsync.cpp
   pitsync1.cpp
   scanedg.cpp
   sortflts.cpp
   strokewidth.cpp
   tabfind.cpp
   tablefind.cpp
   tabvector.cpp
   tablerecog.cpp
   textlineprojection.cpp
   textord.cpp
   topitch.cpp
   tordmain.cpp
   tospace.cpp
   tovars.cpp
   underlin.cpp
   wordseg.cpp
   workingpartset.cpp
)

add_library(tesseract_textord_static STATIC ${tesseract_textord_STAT_SRCS})
include_directories(${CMAKE_SOURCE_DIR}/ccstruct)
include_directories(${CMAKE_SOURCE_DIR}/ccutil)
include_directories(${CMAKE_SOURCE_DIR}/viewer)
include_directories(${CMAKE_SOURCE_DIR}/classify)
include_directories(${CMAKE_SOURCE_DIR}/dict)
include_directories(${CMAKE_SOURCE_DIR}/wordrec)
include_directories(${CMAKE_SOURCE_DIR}/cutil)
include_directories(${CMAKE_SOURCE_DIR}/neural_networks/runtime)
include_directories(${CMAKE_SOURCE_DIR}/cube)
include_directories(${CMAKE_SOURCE_DIR}/textord)
include_directories(${CMAKE_SOURCE_DIR}/opencl)
include_directories(${CMAKE_SOURCE_DIR}/ccmain)
include_directories(${CMAKE_SOURCE_DIR}/msvsport)

########### next target ###############

SET(tesseract_main_STAT_SRCS
   adaptions.cpp
   applybox.cpp
   control.cpp
   cube_control.cpp
   cube_reco_context.cpp
   cubeclassifier.cpp
   docqual.cpp
   equationdetect.cpp
   fixspace.cpp
   fixxht.cpp
   ltrresultiterator.cpp
   osdetect.cpp
   output.cpp
   pageiterator.cpp
   pagesegmain.cpp
   pagewalk.cpp
   par_control.cpp
   paragraphs.cpp
   paramsd.cpp
   pgedit.cpp
   recogtraining.cpp
   reject.cpp
   resultiterator.cpp
   superscript.cpp
   tesseract_cube_combiner.cpp
   tessbox.cpp
   tessedit.cpp
   tesseractclass.cpp
   tessvars.cpp
   tfacepp.cpp
   thresholder.cpp
   werdit.cpp
)

add_library(tesseract_main_static STATIC ${tesseract_main_STAT_SRCS})

########### install files ###############

install(
    FILES
        thresholder.h
        ltrresultiterator.h
        pageiterator.h
        resultiterator.h
        osdetect.h
    DESTINATION
        include/tesseract
)
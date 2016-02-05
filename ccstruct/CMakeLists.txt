include_directories(${CMAKE_SOURCE_DIR}/ccutil)
include_directories(${CMAKE_SOURCE_DIR}/viewer)
include_directories(${CMAKE_SOURCE_DIR}/cutil)
include_directories(${CMAKE_SOURCE_DIR}/opencl)

########### next target ###############

SET(tesseract_ccstruct_STAT_SRCS
   blamer.cpp
   blobbox.cpp
   blobs.cpp
   blread.cpp
   boxread.cpp
   boxword.cpp
   ccstruct.cpp
   coutln.cpp
   detlinefit.cpp
   dppoint.cpp
   fontinfo.cpp
   genblob.cpp
   linlsq.cpp
   matrix.cpp
   mod128.cpp
   normalis.cpp
   ocrblock.cpp
   ocrpara.cpp
   ocrrow.cpp
   otsuthr.cpp
   pageres.cpp
   pdblock.cpp
   points.cpp
   polyaprx.cpp
   polyblk.cpp
   params_training_featdef.cpp
   publictypes.cpp
   quadlsq.cpp
   quspline.cpp
   ratngs.cpp
   rect.cpp
   rejctmap.cpp
   seam.cpp
   split.cpp
   statistc.cpp
   stepblob.cpp
   vecfuncs.cpp
   werd.cpp
)

add_library(tesseract_ccstruct_static STATIC ${tesseract_ccstruct_STAT_SRCS})

########### install files ###############

install(
    FILES
        publictypes.h
    DESTINATION
        include/tesseract
)
include_directories(${CMAKE_SOURCE_DIR}/ccstruct)
include_directories(${CMAKE_SOURCE_DIR}/ccutil)
include_directories(${CMAKE_SOURCE_DIR}/cutil)
include_directories(${CMAKE_SOURCE_DIR}/viewer)
include_directories(${CMAKE_SOURCE_DIR}/classify)
include_directories(${CMAKE_SOURCE_DIR}/dict)

########### next target ###############

SET(tesseract_wordrec_STAT_SRCS
   associate.cpp
   chop.cpp
   chopper.cpp
   drawfx.cpp
   findseam.cpp
   gradechop.cpp
   language_model.cpp
   lm_consistency.cpp
   lm_pain_points.cpp
   lm_state.cpp
   makechop.cpp
   olutil.cpp
   outlines.cpp
   params_model.cpp
   pieces.cpp
   plotedges.cpp
   render.cpp
   segsearch.cpp
   tface.cpp
   wordclass.cpp
   wordrec.cpp
)

add_library(tesseract_wordrec_static STATIC ${tesseract_wordrec_STAT_SRCS})
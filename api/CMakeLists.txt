include_directories(${CMAKE_SOURCE_DIR}/ccutil)
include_directories(${CMAKE_SOURCE_DIR}/ccstruct)
include_directories(${CMAKE_SOURCE_DIR}/cube)
include_directories(${CMAKE_SOURCE_DIR}/viewer)
include_directories(${CMAKE_SOURCE_DIR}/textord)
include_directories(${CMAKE_SOURCE_DIR}/dict)
include_directories(${CMAKE_SOURCE_DIR}/classify)
include_directories(${CMAKE_SOURCE_DIR}/ccmain)
include_directories(${CMAKE_SOURCE_DIR}/wordrec)
include_directories(${CMAKE_SOURCE_DIR}/cutil)
include_directories(${CMAKE_SOURCE_DIR}/opencl)
include_directories(${CMAKE_SOURCE_DIR}/msvsport)

########### next target ###############

SET(tesseract_api_STAT_SRCS
   baseapi.cpp
   capi.cpp
   pdfrenderer.cpp
   renderer.cpp
)

add_library(tesseract_api_static STATIC ${tesseract_api_STAT_SRCS})
target_link_libraries(tesseract_api_static
    tesseract_main_static
    )

########### install files ###############

install(
    FILES
        apitypes.h baseapi.h capi.h renderer.h
    DESTINATION
        include/tesseract
)
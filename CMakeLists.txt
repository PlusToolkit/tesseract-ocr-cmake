project(tesseract-ocr)
cmake_minimum_required(VERSION 3.0.0)

SET(tesseract_VERSION_MAJOR     3)
SET(tesseract_VERSION_MINOR     3)
SET(tesseract_VERSION           ${tesseract_VERSION_MAJOR}.${tesseract_VERSION_MINOR})

FIND_PACKAGE(Leptonica REQUIRED NO_MODULE PATHS ${Leptonica_DIR})

include_directories(${Leptonica_INCLUDE_DIRS})

add_definitions(-DUSE_STD_NAMESPACE)
if( NOT WIN32 )
  add_definitions(-fPIC)
endif()
add_definitions(-DWINDLLNAME="tesseract")

add_subdirectory(ccutil)
add_subdirectory(viewer)
add_subdirectory(cutil)
add_subdirectory(opencl)
add_subdirectory(ccstruct)
add_subdirectory(dict)
add_subdirectory(classify)
add_subdirectory(wordrec)
add_subdirectory(neural_networks/runtime)
add_subdirectory(textord)
add_subdirectory(cube)
add_subdirectory(ccmain)
add_subdirectory(api)
add_subdirectory(tessdata)
add_subdirectory(doc)
add_subdirectory(msvsport)

list(APPEND tesseract_LIBRARIES
    tesseract_api_static
    tesseract_main_static
    tesseract_cube_static
    tesseract_neural_static
    tesseract_textord_static
    tesseract_wordrec_static
    tesseract_classify_static
    tesseract_dict_static
    tesseract_ccstruct_static
    tesseract_cutil_static
    tesseract_viewer_static
    tesseract_ccutil_static
    tesseract_opencl_static
    tesseract_msvsport_static
)

SET( tesseract_INCLUDE_DIRS ${CMAKE_INSTALL_PREFIX}/include ${Leptonica_INCLUDE_DIRS})

export(TARGETS ${tesseract_LIBRARIES} FILE ${CMAKE_BINARY_DIR}/TesseractTargets.cmake)

SET( tesseract_LIBRARIES ${tesseract_LIBRARIES} ${Leptonica_LIBRARIES} )

# Create a tesseractConfig.cmake file for use from the build tree
CONFIGURE_FILE(tesseractConfig.cmake.in
  "${CMAKE_CURRENT_BINARY_DIR}/tesseractConfig.cmake" @ONLY)
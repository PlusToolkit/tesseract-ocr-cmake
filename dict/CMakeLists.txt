include_directories(${CMAKE_SOURCE_DIR}/cutil)
include_directories(${CMAKE_SOURCE_DIR}/ccutil)
include_directories(${CMAKE_SOURCE_DIR}/ccstruct)
include_directories(${CMAKE_SOURCE_DIR}/viewer)

########### next target ###############

SET(tesseract_dict_STAT_SRCS
   context.cpp
   dawg.cpp
   dawg_cache.cpp
   dict.cpp
   hyphen.cpp
   permdawg.cpp
   stopper.cpp
   trie.cpp
)

add_library(tesseract_dict_static STATIC ${tesseract_dict_STAT_SRCS})
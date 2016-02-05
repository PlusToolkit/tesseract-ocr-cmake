include_directories(${CMAKE_SOURCE_DIR}/cutil)
include_directories(${CMAKE_SOURCE_DIR}/ccutil)
include_directories(${CMAKE_SOURCE_DIR}/ccstruct)
include_directories(${CMAKE_SOURCE_DIR}/dict)
include_directories(${CMAKE_SOURCE_DIR}/viewer)
include_directories(${CMAKE_SOURCE_DIR}/msvsport)

########### next target ###############

SET(tesseract_classify_STAT_SRCS
   adaptive.cpp
   adaptmatch.cpp
   blobclass.cpp
   classify.cpp
   cluster.cpp
   clusttool.cpp
   cutoffs.cpp
   errorcounter.cpp
   extract.cpp
   featdefs.cpp
   flexfx.cpp
   float2int.cpp
   fpoint.cpp
   fxdefs.cpp
   intfeaturedist.cpp
   intfeaturemap.cpp
   intfeaturespace.cpp
   intfx.cpp
   intmatcher.cpp
   intproto.cpp
   kdtree.cpp
   mastertrainer.cpp
   mf.cpp
   mfdefs.cpp
   mfoutline.cpp
   mfx.cpp
   normfeat.cpp
   normmatch.cpp
   ocrfeatures.cpp
   outfeat.cpp
   picofeat.cpp
   protos.cpp
   sampleiterator.cpp
   shapeclassifier.cpp
   shapetable.cpp
   tessclassifier.cpp
   trainingsample.cpp
   trainingsampleset.cpp
   xform2d.cpp
)

add_library(tesseract_classify_static STATIC ${tesseract_classify_STAT_SRCS})
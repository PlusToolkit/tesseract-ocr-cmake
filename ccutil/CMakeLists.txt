
########### next target ###############

SET(tesseract_ccutil_STAT_SRCS
   ambigs.cpp
   basedir.cpp
   bits16.cpp
   bitvector.cpp
   ccutil.cpp
   clst.cpp
   elst2.cpp
   elst.cpp
   errcode.cpp
   globaloc.cpp
   indexmapbidi.cpp
   mainblk.cpp
   memry.cpp
   serialis.cpp
   strngs.cpp
   scanutils.cpp
   tessdatamanager.cpp
   tprintf.cpp
   unichar.cpp
   unicharmap.cpp
   unicharset.cpp
   unicodes.cpp
   params.cpp
   universalambigs.cpp
)

add_library(tesseract_ccutil_static STATIC ${tesseract_ccutil_STAT_SRCS})

########### install files ###############

install(
    FILES
        basedir.h
        errcode.h
        fileerr.h
        genericvector.h
        helpers.h
        host.h
        memry.h
        ndminx.h
        params.h
        ocrclass.h
        platform.h
        serialis.h
        strngs.h
        tesscallback.h
        unichar.h
        unicharmap.h
        unicharset.h
    DESTINATION
        include/tesseract
)
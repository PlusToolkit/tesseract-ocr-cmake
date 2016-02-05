
########### next target ###############

SET(tesseract_training_STAT_SRCS
   boxchar.cpp
   commandlineflags.cpp
   commontraining.cpp
   degradeimage.cpp
   fileio.cpp
   ligature_table.cpp
   normstrngs.cpp
   pango_font_info.cpp
   stringrenderer.cpp
   tlog.cpp
)

add_library(tesseract_training_static STATIC ${tesseract_training_STAT_SRCS})


########### next target ###############

SET(tesseract_tessopt_STAT_SRCS
   tessopt.cpp
)

add_library(tesseract_tessopt_static STATIC ${tesseract_tessopt_STAT_SRCS})


########### next target ###############

SET(ambiguous_words_SRCS
   ambiguous_words.cpp
)

add_executable(ambiguous_words ${ambiguous_words_SRCS})

target_link_libraries(ambiguous_words tesseract_training_static tesseract_tessopt_static)

install(TARGETS ambiguous_words DESTINATION bin)
install(TARGETS ambiguous_words_static DESTINATION bin)


########### next target ###############

SET(classifier_tester_SRCS
   classifier_tester.cpp
)

add_executable(classifier_tester ${classifier_tester_SRCS})

target_link_libraries(classifier_tester tesseract_training_static tesseract_tessopt_static)

install(TARGETS classifier_tester DESTINATION bin)


########### next target ###############

SET(cntraining_SRCS
   cntraining.cpp
)

add_executable(cntraining ${cntraining_SRCS})

target_link_libraries(cntraining tesseract_training_static tesseract_tessopt_static)

install(TARGETS cntraining DESTINATION bin)


########### next target ###############

SET(combine_tessdata_SRCS
   combine_tessdata.cpp
)

add_executable(combine_tessdata ${combine_tessdata_SRCS})

target_link_libraries(combine_tessdata tesseract_ccutil tesseract)

install(TARGETS combine_tessdata DESTINATION bin)


########### next target ###############

SET(dawg2wordlist_SRCS
   dawg2wordlist.cpp
)

add_executable(dawg2wordlist ${dawg2wordlist_SRCS})

target_link_libraries(dawg2wordlist tesseract_tessopt)

install(TARGETS dawg2wordlist DESTINATION bin)


########### next target ###############

SET(mftraining_SRCS
   mftraining.cpp
   mergenf.cpp
)

add_executable(mftraining ${mftraining_SRCS})

target_link_libraries(mftraining tesseract_training tesseract_tessopt)

install(TARGETS mftraining DESTINATION bin)


########### next target ###############

SET(set_unicharset_properties_SRCS
   set_unicharset_properties.cpp
)

add_executable(set_unicharset_properties ${set_unicharset_properties_SRCS})

target_link_libraries(set_unicharset_properties tesseract_training tesseract_tessopt)

install(TARGETS set_unicharset_properties DESTINATION bin)


########### next target ###############

SET(shapeclustering_SRCS
   shapeclustering.cpp
)

add_executable(shapeclustering ${shapeclustering_SRCS})

target_link_libraries(shapeclustering tesseract_training tesseract_tessopt)

install(TARGETS shapeclustering DESTINATION bin)


########### next target ###############

SET(text2image_SRCS
   text2image.cpp
)

add_executable(text2image ${text2image_SRCS})

target_link_libraries(text2image tesseract_training tesseract_tessopt)

install(TARGETS text2image DESTINATION bin)


########### next target ###############

SET(unicharset_extractor_SRCS
   unicharset_extractor.cpp
)

add_executable(unicharset_extractor ${unicharset_extractor_SRCS})

target_link_libraries(unicharset_extractor tesseract_tessopt)

install(TARGETS unicharset_extractor DESTINATION bin)


########### next target ###############

SET(wordlist2dawg_SRCS
   wordlist2dawg.cpp
)

add_executable(wordlist2dawg ${wordlist2dawg_SRCS})

target_link_libraries(wordlist2dawg tesseract_tessopt)

install(TARGETS wordlist2dawg DESTINATION bin)
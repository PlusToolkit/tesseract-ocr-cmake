include_directories(${CMAKE_SOURCE_DIR}/cutil)
include_directories(${CMAKE_SOURCE_DIR}/ccutil)
include_directories(${CMAKE_SOURCE_DIR}/ccmain)
include_directories(${CMAKE_SOURCE_DIR}/ccstruct)
include_directories(${CMAKE_SOURCE_DIR}/viewer)
include_directories(${CMAKE_SOURCE_DIR}/textord)
include_directories(${CMAKE_SOURCE_DIR}/wordrec)
include_directories(${CMAKE_SOURCE_DIR}/classify)
include_directories(${CMAKE_SOURCE_DIR}/dict)
include_directories(${CMAKE_SOURCE_DIR}/neural_networks/runtime)
include_directories(${CMAKE_SOURCE_DIR}/cube)
include_directories(${CMAKE_SOURCE_DIR}/msvsport)

########### next target ###############

SET(tesseract_cube_STAT_SRCS
   altlist.cpp
   beam_search.cpp
   bmp_8.cpp
   cached_file.cpp
   char_altlist.cpp
   char_bigrams.cpp
   char_samp.cpp
   char_samp_enum.cpp
   char_samp_set.cpp
   char_set.cpp
   classifier_factory.cpp
   con_comp.cpp
   conv_net_classifier.cpp
   cube_line_object.cpp
   cube_line_segmenter.cpp
   cube_object.cpp
   cube_search_object.cpp
   cube_tuning_params.cpp
   cube_utils.cpp
   feature_bmp.cpp
   feature_chebyshev.cpp
   feature_hybrid.cpp
   hybrid_neural_net_classifier.cpp
   search_column.cpp
   search_node.cpp
   tess_lang_mod_edge.cpp
   tess_lang_model.cpp
   word_altlist.cpp
   word_list_lang_model.cpp
   word_size_model.cpp
   word_unigrams.cpp
)

add_library(tesseract_cube_static STATIC ${tesseract_cube_STAT_SRCS})